### teste Repository
This is an TEST of git Repository
Testing this to use take notes about code

## TypeScript 

```ts
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

function getName (firstName: string, lastName?: string): string {
  if(lastName == undefined) {
    return firstName;
  }
  return firstName + " " + lastName;
}

console.log(getName('John'));
```
