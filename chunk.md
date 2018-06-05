function chunk(array, length){

  var copiedArray = array.slice();
  var resultArray = [];
	
  const rest = (array.length+1)%length;
  //если без остатка
  if (rest != 0){
  	const steps = (array.length+1)/length + 1;
    const notEven = True;
    alert(steps);
    
    
  }
  else{
    const steps = (array.length+1)%length;
    alert(array.length);
    alert(steps);
  }
  
  for (let i = 0; i <= steps; i++){
    if (!(notEven)){
      resultArray.push(copiedArray.slice(i*length, (i+1)*lendth));
    }
    else{
      resultArray.push(copiedArray.slice(i*length, copiedArray.length));
    }
  }
  return resultArray;
}


alert(chunk([1, 2, 3, 4], 2)) //--> [[ 1, 2], [3, 4]]
alert(chunk([1, 2, 3, 4, 5], 2)) //--> [[ 1, 2], [3, 4], [5]]
alert(chunk([1, 2, 3, 4, 5, 6, 7, 8], 3)) //--> [[ 1, 2, 3], [4, 5, 6], [7, 8]]
alert(chunk([1, 2, 3, 4, 5], 4)) //--> /[[ 1, 2, 3, 4], [5]]
alert(chunk([1, 2, 3, 4, 5], 10)) //--> [[ 1, 2, 3, 4, 5]]