---
layout: page
title: "Base Repository"
category: dive
date: 2014-11-19 13:37:06
---

Conductor comes with a base repository class that you can extend from to get basic CRUD functionality for your models. 
<br /><br />

####Extending the class####


You can extend the base repository class like so


```
use Foo\Models\FooModel;
use Conductor\Core\Repository\BaseEloquentRepository; 

class FooEloquentRepository extends BaseEloquentRepository {

  function __construct(FooModel $foo)
  {
      parent::__construct($foo); 
  }

}
```

<br /><br />
####Available methods####
<br />

```
getAll()
```

Get all records
<br /><br />

```
getAllWithRelationships(array $relationship)
```
Get all records with relationships
<br /><br />

```
find($id)
```
Find one record by id
<br /><br />

```
findBy($field, $value)
```
Find by field with value
<br /><br />

```
findWithRelationships($id, array $relationships)
```
Find by id with relationships
<br /><br />

```
create(array $data)
```
Create with array data
<br /><br />

```
update($id, array $data)
```
Update record with data
<br /><br />

```
destroy($id)
```
Destroy record with id
<br /><br />

```
destroyFromArray(array $id)
```
Destory records from array of ids