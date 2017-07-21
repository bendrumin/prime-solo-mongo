# prime-solo-mongo

# prime-solo-mongo

1

```
db.createCollection('orders')
```

//2


```sql
db.getCollection('orders').insert({
  orderDate: new Date ("2017-02-03"),
  orderTotal: 5.00,
  lineItem: [ {unitPrice: 242, quantity: 1, productName: "Super mega awesome wasp suit"} ],
  lineItem: [ {unitPrice: 2333, quantity: 4, productName: "Mach II Iron Man Suit"} ],
  lineItem: [ {unitPrice: 9, quantity: 1, productName: "My little pony doll"} ]
  });

db.getCollection('orders').insert({
  orderDate: new Date ("2017-04-04"),
  orderTotal: 8000,
  lineItem: [ {unitPrice: 1, quantity: 4, productName: "A log"} ],
  lineItem: [ {unitPrice: 2, quantity: 5, productName: "Two pandas"} ],
  lineItem: [ {unitPrice: 3, quantity: 6, productName: "Front Teeth"} ]

  });
db.getCollection('orders').insert({
  orderDate: new Date ("2017-01-02"),
  orderTotal: 8.00,
  lineItem: [ {unitPrice: 44, quantity: 6, productName: "Pocket Squares"} ],
  lineItem: [ {unitPrice: 1, quantity: 6, productName: "Bill Nye costumes"} ],
  lineItem: [ {unitPrice: 1, quantity: 6, productName: "iPhone 7 Plus"} ]

  });
```

3//

```sql
db.getCollection('orders').find({}).pretty()
```

4//

```sql
db.getCollection('orders').find({orderDate: {$gt: new Date('2017-01-31')}})
```

5//

```sql
db.getCollection('orders').update({orderDate: new Date("2017-02-03")}, {$set: {orderTotal: 63}});
```

6//

```sql
db.getCollection('orders').update({
    orderDate: new Date("2017-02-03")},
    {$push: {lineItem: {unitPrice: 12, quantity: 1, productName: "LED suspenders"}}}
);
```

7//

