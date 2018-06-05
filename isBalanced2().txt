Реализуйте функцию isBalanced2(). Она похожа на функцию isBalanced() из предыдущей группы заданий, но поддерживает три типа скобок: фигурные {}, квадратные [], и круглые (). При передаче функции строки, в которой имеются неправильные скобочные последовательности, функция должна возвращать false.

isBalanced2('(foo { bar (baz) [boo] })') // true
isBalanced2('foo { bar { baz }')         // false
isBalanced2('foo { (bar [baz] } )')      // false



alert(isBalanced2('(foo { bar (baz) [boo] })') )// true
alert(isBalanced2('foo { bar { baz }')       )  // false
alert(isBalanced2('foo { (bar [baz] } )')    )  // false

function isBalanced2(str){
	let res = [];
	for (const char of str){
  	if (['{', '}', '[', ']', '(', ')'].indexOf(char) !== -1){
    	res.push(char);
    }
  }
  
  if (['{', '[', '('].indexOf(res[0]) === -1){ return false }
  if (res.length%2===1){ return false }
  
  for (let i = 0; i<res.length; i++){
  
  	let indexI = ['{', '[', '('].indexOf(res[i]);
    
  	if ( indexI !== -1){
    
    	let right = 0;
      
    	for (let k = i+1; k<res.length; k += 2){
      
      	//let indexK = ['}', ']', ')'].indexOf(res[k]);
        //let rightlist = 
      	if (res[k] === ['}', ']', ')'][indexI]){
        	right++;
        }
        
      }
      if (right === 0){
      	return false;
      }
    }
  }
  return true
}