Реализуйте функцию isSorted(), которая возвращает true или false в зависимости о того, отсортирован ли переданный ей числовой массив.

isSorted([])                        // true
isSorted([-Infinity, -5, 0, 3, 9])  // true
isSorted([3, 9, -3, 10])            // false

alert(isSorted([])    );                    // true
alert(isSorted([-Infinity, -5, 0, 3, 9])  );     // true
alert(isSorted([3, 9, -3, 10])           );      // false

function isSorted(arr){
  var copy = arr.slice();
  //alert(arr);
  
  copy.sort((a, b)=> a>b);
  for (let i = 0; i<=arr.length-1; i++){
  	if (arr[i] !== copy[i]){
    	return false
    }
  }
  return true