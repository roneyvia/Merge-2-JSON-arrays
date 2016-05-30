# Merge-2-JSON-arrays

Example

```javascript
var array1 = [{
  box: 123,
  name: 'name123',
  amount: 'amount123'
}, {
  box: 321,
  name: 'name321',
  amount: 'amount321'
}, {
  box: 789,
  name: 'name789',
  amount: 'amount789'
}];

var array2 = [{
  _id: 123,
  look: 'look123',
  title: 'title123'
}, {
  _id: 321,
  look: 'look321',
  title: 'title321'
}];

var newArray = [];
for (var i = 0; i < array1.length; i++) {
  var obj = array1[i];
	if (array2[i] && obj.box == array2[i]._id) {
  	for (key in array2[i]) {
      obj[key] = array2[i][key];
    }
    newArray.push(obj);
  }
};

alert(newObj);

```
