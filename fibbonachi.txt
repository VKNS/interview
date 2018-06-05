Реализуйте функцию fib2(). Она похожа на функцию fib() из предыдущей группы заданий, но поддерживает числа вплоть до 50. Подсказка: используйте мемоизацию.

fib2(0)                               // 0
fib2(1)                               // 1
fib2(10)                              // 55
fib2(50)                              // 12586269025



alert(fib2(0)    ) // 0
alert(fib2(1) )// 1
alert(fib2(10))  // 55
alert(fib2(50)     )  // 12586269025


function fib2(num){
	let numList = [];
  for (let i=0; i<=num; i++){
  		numList.push(i)
  }
  //let cash = {};
  let fib = numList.reduce(function(acc, num, i){
  	//cash[i] = acc+num;
  	return acc+num
  })/*
  for (let fib in cash){
  	console.log(fib+':  '+cash[fib])
  }*/
  
  return fib;
}