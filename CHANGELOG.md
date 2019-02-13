# Changelog

TypeORM follows a semantic versioning and until `1.0.0` breaking changes may appear in `0.x.x` versions,
however since API is already quite stable we don't expect too much breaking changes.
If we missed a note on some change or you have a questions on migrating from old version,
feel free to ask us and community.

## 0.2.13 (2019-02-10)

### Bug Fixes

* fixed undefined object id field in case property name is `_id` ([3517](https://github.com/typeorm/typeorm/issues/3517))
* allow to use mongodb index options in `Index` decorator ([#3592](https://github.com/typeorm/typeorm/pull/3592))
* fixed entity embeddeds indices in mongodb ([#3585](https://github.com/typeorm/typeorm/pull/3585))
* fixed json/jsonb column data types comparison ([#3496](https://github.com/typeorm/typeorm/issues/3496))
* fixed increment/decrement value of embedded entity ([#3182](https://github.com/typeorm/typeorm/issues/3182))
* fixed missing call `transformer.from()` in case column is NULL ([#3395](https://github.com/typeorm/typeorm/issues/3395))
* fixed signatures of `update`/`insert` methods, some `find*` methods in repositories, entity managers, BaseEntity and QueryBuilders
* handle embedded documents through multiple levels in mongodb ([#3551](https://github.com/typeorm/typeorm/issues/3551))
* fixed hanging connections in `mssql` driver ([#3327](https://github.com/typeorm/typeorm/pull/3327))

### Features

* Injection 2nd parameter(options) of constructor to `ioredis/cluster` is now possible([#3538](https://github.com/typeorm/typeorm/issues/3538))

## 0.2.12 (2019-01-20)

### Bug Fixes

* fixed mongodb entity listeners and subscribers ([#1527](https://github.com/typeorm/typeorm/issues/1527))
* fixed connection options builder - paramters parsed from url are assigned on top of options ([#3442](https://github.com/typeorm/typeorm/pull/3442))
* fixed issue with logical operator precedence in `QueryBuilder` `whereInIds` ([#2103](https://github.com/typeorm/typeorm/issues/2103))
* fixed missing `isolationLevel` in `Connection.transaction()` method ([#3363](https://github.com/typeorm/typeorm/issues/3363))
* fixed broken findOne method with custom join column name
* fixed issue with uuid in mysql ([#3374](https://github.com/typeorm/typeorm/issues/3374))
* fixed missing export of `Exclusion` decorator
* fixed ignored extra options in mongodb driver ([#3403](https://github.com/typeorm/typeorm/pull/3403), [#1741](https://github.com/typeorm/typeorm/issues/1741))
* fixed signature of root `getRepository` function to accept `EntitySchema<Entity>` ([#3402](https://github.com/typeorm/typeorm/pull/3402))
* fixed false undefined connection options passed into mongodb client ([#3366](https://github.com/typeorm/typeorm/pull/3366))
* fixed ER_DUP_FIELDNAME with simple find ([#3350](https://github.com/typeorm/typeorm/issues/3350))
