# Failed applyMigration at 2019-08-05T20:01:40.729Z
## RPC Input One Line
```json
{"id":1,"jsonrpc":"2.0","method":"applyMigration","params":{"projectInfo":"","force":false,"migrationId":"20190806013049-add-post","steps":[{"stepType":"CreateModel","name":"User","embedded":false},{"stepType":"CreateField","model":"User","name":"id","type":{"Base":"String"},"arity":"required","isUnique":true,"id":{"strategy":"Auto","sequence":null},"default":{"Expression":["cuid","String",[]]}},{"stepType":"CreateField","model":"User","name":"email","type":{"Base":"String"},"arity":"required","isUnique":true},{"stepType":"CreateField","model":"User","name":"name","type":{"Base":"String"},"arity":"optional","isUnique":false},{"stepType":"CreateModel","name":"Post","embedded":false},{"stepType":"CreateField","model":"User","name":"posts","type":{"Relation":{"to":"Post","to_fields":[],"name":"PostToUser","on_delete":"None"}},"arity":"list","isUnique":false},{"stepType":"CreateField","model":"Post","name":"id","type":{"Base":"String"},"arity":"required","isUnique":true,"id":{"strategy":"Auto","sequence":null},"default":{"Expression":["cuid","String",[]]}},{"stepType":"CreateField","model":"Post","name":"createdAt","type":{"Base":"DateTime"},"arity":"required","isUnique":false,"default":{"Expression":["now","DateTime",[]]}},{"stepType":"CreateField","model":"Post","name":"updatedAt","type":{"Base":"DateTime"},"arity":"required","isUnique":false},{"stepType":"CreateField","model":"Post","name":"published","type":{"Base":"Boolean"},"arity":"required","isUnique":false},{"stepType":"CreateField","model":"Post","name":"title","type":{"Base":"String"},"arity":"required","isUnique":false},{"stepType":"CreateField","model":"Post","name":"content","type":{"Base":"String"},"arity":"optional","isUnique":false},{"stepType":"CreateField","model":"Post","name":"author","type":{"Relation":{"to":"User","to_fields":["id"],"name":"PostToUser","on_delete":"None"}},"arity":"optional","isUnique":false}],"sourceConfig":"datasource db {\n  provider = \"sqlite\"\n  url      = \"file:dev.db\"\n  default  = true\n}\n\ngenerator photon {\n  provider = \"photonjs\"\n}\n\nmodel User {\n  id    String  @default(cuid()) @id @unique\n  email String  @unique\n  name  String?\n  posts Post[]\n}\n\nmodel Post {\n  id        String   @default(cuid()) @id @unique\n  createdAt DateTime @default(now())\n  updatedAt DateTime @updatedAt\n  published Boolean\n  title     String\n  content   String?\n  author    User?\n}"}}
```

## RPC Input Readable
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "applyMigration",
  "params": {
    "projectInfo": "",
    "force": false,
    "migrationId": "20190806013049-add-post",
    "steps": [
      {
        "stepType": "CreateModel",
        "name": "User",
        "embedded": false
      },
      {
        "stepType": "CreateField",
        "model": "User",
        "name": "id",
        "type": {
          "Base": "String"
        },
        "arity": "required",
        "isUnique": true,
        "id": {
          "strategy": "Auto",
          "sequence": null
        },
        "default": {
          "Expression": [
            "cuid",
            "String",
            []
          ]
        }
      },
      {
        "stepType": "CreateField",
        "model": "User",
        "name": "email",
        "type": {
          "Base": "String"
        },
        "arity": "required",
        "isUnique": true
      },
      {
        "stepType": "CreateField",
        "model": "User",
        "name": "name",
        "type": {
          "Base": "String"
        },
        "arity": "optional",
        "isUnique": false
      },
      {
        "stepType": "CreateModel",
        "name": "Post",
        "embedded": false
      },
      {
        "stepType": "CreateField",
        "model": "User",
        "name": "posts",
        "type": {
          "Relation": {
            "to": "Post",
            "to_fields": [],
            "name": "PostToUser",
            "on_delete": "None"
          }
        },
        "arity": "list",
        "isUnique": false
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "id",
        "type": {
          "Base": "String"
        },
        "arity": "required",
        "isUnique": true,
        "id": {
          "strategy": "Auto",
          "sequence": null
        },
        "default": {
          "Expression": [
            "cuid",
            "String",
            []
          ]
        }
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "createdAt",
        "type": {
          "Base": "DateTime"
        },
        "arity": "required",
        "isUnique": false,
        "default": {
          "Expression": [
            "now",
            "DateTime",
            []
          ]
        }
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "updatedAt",
        "type": {
          "Base": "DateTime"
        },
        "arity": "required",
        "isUnique": false
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "published",
        "type": {
          "Base": "Boolean"
        },
        "arity": "required",
        "isUnique": false
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "title",
        "type": {
          "Base": "String"
        },
        "arity": "required",
        "isUnique": false
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "content",
        "type": {
          "Base": "String"
        },
        "arity": "optional",
        "isUnique": false
      },
      {
        "stepType": "CreateField",
        "model": "Post",
        "name": "author",
        "type": {
          "Relation": {
            "to": "User",
            "to_fields": [
              "id"
            ],
            "name": "PostToUser",
            "on_delete": "None"
          }
        },
        "arity": "optional",
        "isUnique": false
      }
    ],
    "sourceConfig": "datasource db {\n  provider = \"sqlite\"\n  url      = \"file:dev.db\"\n  default  = true\n}\n\ngenerator photon {\n  provider = \"photonjs\"\n}\n\nmodel User {\n  id    String  @default(cuid()) @id @unique\n  email String  @unique\n  name  String?\n  posts Post[]\n}\n\nmodel Post {\n  id        String   @default(cuid()) @id @unique\n  createdAt DateTime @default(now())\n  updatedAt DateTime @updatedAt\n  published Boolean\n  title     String\n  content   String?\n  author    User?\n}"
  }
}
```


## RPC Response
```
null
```

## Stack Trace
```bash
thread 'main' panicked at 'The model User already exists in this Datamodel. It is not possible to create it once more.', migration-engine/core/src/migration/datamodel_calculator.rs:59:9
stack backtrace:
   0: std::sys::unix::backtrace::tracing::imp::unwind_backtrace
   1: std::sys_common::backtrace::_print
   2: std::panicking::default_hook::{{closure}}
   3: std::panicking::default_hook
   4: std::panicking::rust_panic_with_hook
   5: std::panicking::continue_panic_fmt
   6: std::panicking::begin_panic_fmt
   7: <migration_core::migration::datamodel_calculator::DataModelCalculatorImpl as migration_core::migration::datamodel_calculator::DataModelCalculator>::infer
   8: <migration_core::commands::apply_migration::ApplyMigrationCommand as migration_core::commands::command::MigrationCommand>::execute
   9: <F as jsonrpc_core::calls::RpcMethodSimple>::call
  10: <F as jsonrpc_core::calls::RpcMethod<T>>::call
  11: <futures::future::lazy::Lazy<F,R> as futures::future::Future>::poll
  12: <futures::future::then::Then<A,B,F> as futures::future::Future>::poll
  13: <futures::future::map::Map<A,F> as futures::future::Future>::poll
  14: <futures::future::either::Either<A,B> as futures::future::Future>::poll
  15: futures::task_impl::std::set
  16: std::thread::local::LocalKey<T>::with
  17: futures::future::Future::wait
  18: jsonrpc_core::io::IoHandler<M>::handle_request_sync
  19: migration_core::rpc_api::RpcApi::handle
  20: migration_engine::main
  21: std::rt::lang_start::{{closure}}
  22: std::panicking::try::do_call
  23: __rust_maybe_catch_panic
  24: std::rt::lang_start_internal
  25: main

```
