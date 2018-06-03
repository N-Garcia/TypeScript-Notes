# testeRepository
This is an TEST of git Repository

TypeScript 

let mySum = function(num1: any, num2:any):number {
  if (tyopeof num1 == 'string') {
    num1 = parseInt(num1);
  }
  if (typeof num2 == 'string') {
    num2 = parseInt(num2);
  }
  return num1 + num2;
}

console.log(mySum('3',5));

