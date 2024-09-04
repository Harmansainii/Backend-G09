Current Mongosh Log ID:	66d89c77ae0a3173e9c8aee6
Connecting to:		mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.3.0
Using MongoDB:		7.0.14
Using Mongosh:		2.3.0

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

------
   The server generated these startup warnings when booting
   2024-09-04T22:52:50.390+05:30: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
------

test> class
ReferenceError: class is not defined
test> show dbs
admin   40.00 KiB
config  72.00 KiB
local   72.00 KiB
test> use class
switched to db class
class> db.createCollection
[Function: createCollection] AsyncFunction {
  apiVersions: [ 1, Infinity ],
  returnsPromise: true,
  serverVersions: [ '0.0.0', '999.999.999' ],
  topologies: [ 'ReplSet', 'Sharded', 'LoadBalanced', 'Standalone' ],
  returnType: { type: 'unknown', attributes: {} },
  deprecated: false,
  platforms: [ 'Compass', 'Browser', 'CLI' ],
  isDirectShellCommand: false,
  acceptsRawInput: false,
  shellCommandCompleter: undefined,
  help: [Function (anonymous)] Help
}
class> db.userinsertMany
class.userinsertMany
class> db.createCollection("Student")
{ ok: 1 }
class> db.user.insertMany([{name:"Jack",age:20,marks:85,subject :"Mathematcis"},{name:"Bob",age:22,marks:78,subject:"Physics"},{name:"Nav",age:21,marks:92,subject:"Chemistry"},{name:"Hitesh",age:19,marks:90,subject:"Chemistry"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d152553216c2185a2710bc'),
    '1': ObjectId('66d152553216c2185a2710bd'),
    '2': ObjectId('66d152553216c2185a2710be'),
    '3': ObjectId('66d152553216c2185a2710bf')
  }
}
class> db.createCollection("Faculty")
{ ok: 1 }
class> db.Student.insertMany([{name:"Jaiko",age:60,rating:85,subject :"Mathematcis"},{name:"Boby",age:82,rating:78,subjclass> db.Student.insertMany([{name:"Jaiko",age:60,rating:85,subject :"Mathematcis"},{name:"Boby",age:82,rating:78,subject:"Physics"},{name:"Naiv",age:56,rating:92,subject:"Chemistry"},{name:"CHinky",age:45,rating:90,subject:"Chemistry"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d152963216c2185a2710c0'),
    '1': ObjectId('66d152963216c2185a2710c1'),
    '2': ObjectId('66d152963216c2185a2710c2'),
    '3': ObjectId('66d152963216c2185a2710c3')
  }
}
class> db.Faculty.insertMany([{name:"Jaiko",age:60,rating:85,subject :"Mathematcis"},{name:"Boby",age:82,rating:78,subjclass> db.Faculty.insertMany([{name:"Jaiko",age:60,rating:85,subject :"Mathematcis"},{name:"Boby",age:82,rating:78,subject:"Physics"},{name:"Naiv",age:56,rating:92,subject:"Chemistry"},{name:"CHinky",age:45,rating:90,subject:"Chemistry"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('66d152fa3216c2185a2710c4'),
    '1': ObjectId('66d152fa3216c2185a2710c5'),
    '2': ObjectId('66d152fa3216c2185a2710c6'),
    '3': ObjectId('66d152fa3216c2185a2710c7')
  }
}
class> db.user.countDocuments()
4
class> db.Faculty.countDocuments()
4
class> db.student.estimatedDocumentCount()
0
class> db.user.insertOne({date:ISODate()});
{
  acknowledged: true,
  insertedId: ObjectId('66d153b63216c2185a2710c8')
}
class> db.user.find().pretty();
[
  {
    _id: ObjectId('66d152553216c2185a2710bc'),
    name: 'Jack',
    age: 20,
    marks: 85,
    subject: 'Mathematcis'
  },
  {
    _id: ObjectId('66d152553216c2185a2710bd'),
    name: 'Bob',
    age: 22,
    marks: 78,
    subject: 'Physics'
  },
  {
    _id: ObjectId('66d152553216c2185a2710be'),
    name: 'Nav',
    age: 21,
    marks: 92,
    subject: 'Chemistry'
  },
  {
    _id: ObjectId('66d152553216c2185a2710bf'),
    name: 'Hitesh',
    age: 19,
    marks: 90,
    subject: 'Chemistry'
  },
  {
    _id: ObjectId('66d153b63216c2185a2710c8'),
    date: ISODate('2024-08-30T05:08:06.347Z')
  }
]
class> db.user.findOne();
{
  _id: ObjectId('66d152553216c2185a2710bc'),
  name: 'Jack',
  age: 20,
  marks: 85,
  subject: 'Mathematcis'
}
class> db.student.updateMany({},{$set:{Student:"DataScience",address:"Chitkara University"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
class> db.students.bulkWrite([{updateOne: { filter: { name: "Jack" },   update: { $set: { grade: "A" } } } }, {    updaupdateOne: {filter: { name: "Bob" }, update: { $set: { grade: "B" } } } }, {updateOne: {filter: { name: "Nav" },
...       update: { $set: { grade: "A+" } }
...     }
...   },
...   {
...     updateOne: {
...       filter: { name: "Illu" },
...       update: { $set: { grade: "B+" } }
...     }
...   },
...   {
...     updateOne: {
...       filter: { name: "Eva" },
...       update: { $set: { grade: "A" } }
...     }
...   }
...
...
...   }
class> db.students.bulkWrite([{updateOne: { filter: { name: "Jack" },   update: { $set: { grade: "A" } } } }, {    updaupdateOne: {filter: { name: "Bob" }, update: { $set: { grade: "B" } } } }, {updateOne: {filter: { name: "Nav" },
...       update: { $set: { grade: "A+" } }
...     }
...   },
...   {
...     updateOne: {
...       filter: { name: "Illu" },
...       update: { $set: { grade: "B+" } }
...     }
...   },
...   {
...     updateOne: {
...       filter: { name: "Eva" },
...       update: { $set: { grade: "A" } }
...     }
...   }
...
class> db.Student.bulkWrite([{updateOne:{filter:{name:"Jaiko"},update:{$set:{grade:"A"}}}},updateOne:{filter:{name:"Bobclass> db.Student.bulkWrite([{updateOne:{filter:{name:"Jaiko"},update:{$set:{grade:"A"}}}},updateOne:{filter:{name:"Boby"},update:{$set:{grade:"B"}}}},{db.students.bulkWrite([{updateOne: { filter: { name: "Jack" },   update: { $set: { grade: "A" } } } }, {    updateOne: {filter: { name: "Bob" }, update: { $set: { grade: "B" } } } }, {updateOne: {filter: { nname: "Nav" },
Uncaught:
SyntaxError: Unexpected token, expected "," (1:93)

> 1 | db.Student.bulkWrite([{updateOne:{filter:{name:"Jaiko"},update:{$set:{grade:"A"}}}},updateOne:{filter:{name:"Boby"},update:{$set:{grade:"B"}}}},{db.students.bulkWrite([{updateOne: { filter: { name: "Jack" },   update: { $set: { grade: "A" } } } }, {    updateOne: {filter: { name: "Bob" }, update: { $set: { grade: "B" } } } }, {updateOne: {filter: { name: "Nav" },
    |                                                                                              ^
  2 |

class>       update: { $set: { grade: "A+" } }
A+
class>     }
Uncaught:
SyntaxError: Unexpected token (1:4)

> 1 |     }
    |     ^
  2 |

class>   },
Uncaught:
SyntaxError: Unexpected token (1:2)

> 1 |   },
    |   ^
  2 |

class>   {
...     updateOne: {
...       filter: { name: "Illu" },
...       update: { $set: { grade: "B+" } }
...     }
...   },
...   {
...     updateOne: {
...       filter: { name: "Eva" },
...       update: { $set: { grade: "A" } }
...     }
...   }
class> db.Student.bulkWrite([{updateOne:{filter:{name:"Jaiko"},update:{$set:{grade:"A"}}}},updateOne:{filter:{name:"Boby"},update:{$set:{grade:"B"}}}},{updateOne: {filter:{name:"Naiv"},update:{$set:{grade:"A+"}}}},{updateOne:{filter:{name:"Chinky"},update:{$set:{grade:"A"}}}}])
Uncaught:
SyntaxError: Unexpected token, expected "," (1:93)

> 1 | db.Student.bulkWrite([{updateOne:{filter:{name:"Jaiko"},update:{$set:{grade:"A"}}}},updateOne:{filter:{name:"Boby"},update:{$set:{grade:"B"}}}},{updateOne: {filter:{name:"Naiv"},update:{$set:{grade:"A+"}}}},{updateOne:{filter:{name:"Chinky"},update:{$set:{grade:"A"}}}}])
    |                                                                                              ^
  2 |

class> db.Student.bulkWrite([
...     { updateOne: { filter: { name: "Jaiko" }, update: { $set: { grade: "A" } } } },
...     { updateOne: { filter: { name: "Boby" }, update: { $set: { grade: "B" } } } },
...     { updateOne: { filter: { name: "Naiv" }, update: { $set: { grade: "A+" } } } },
...     { updateOne: { filter: { name: "Chinky" }, update: { $set: { grade: "A" } } } }
... ]);
{
  acknowledged: true,
  insertedCount: 0,
  insertedIds: {},
  matchedCount: 3,
  modifiedCount: 3,
  deletedCount: 0,
  upsertedCount: 0,
  upsertedIds: {}
}
class> db.Student.bulkWrite([ { updateOne: { filter: { name: "Jaiko" }, update: { $set: { grade: "A" } } } }, { updateOne: { filter: { name: "Boby" }, update: { $set: { grade: "B" } } } }, { updateOne: { filter: { name: "Naiv" }, update: { $set: { grade: "A+" } } } }, { updateOne: { filter: { name: "CHinky" }, update: { $set: { grade: "A" } } } }] );
{
  acknowledged: true,
  insertedCount: 0,
  insertedIds: {},
  matchedCount: 4,
  modifiedCount: 1,
  deletedCount: 0,
  upsertedCount: 0,
  upsertedIds: {}
}
class> db.Student.find({ age: 22, marks: 90 })

class>

class> db.Student.find({ age: 22, marks: 90 })

class> db.user.find({ age: 22, marks: 90 })

class> db.Student.find({ grade: "A+" })
[
  {
    _id: ObjectId('66d152963216c2185a2710c2'),
    name: 'Naiv',
    age: 56,
    rating: 92,
    subject: 'Chemistry',
    grade: 'A+'
  }
]
class> -->