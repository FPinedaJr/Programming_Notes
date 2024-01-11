- A small section of code that gets executed when it is called.

main function:
```c
int main(){
	code...
	code...
	code...
	return 0;
}
```

invoking a function:
```c
void functionName(){
	code...
	code...
	code...
	code...
}
```
calling a function:
```c
functionName();
```
**NOTE!** this will not return anything since it is void. It also has no parameters.

## arguments and parameters
```c
void greeting(char x[]){
	printf("\nHello, %s", x);
}
int main(){
	char name[] = "meow";
	greeting(name);
}
```
In this case `char x[]` is an parameter while the name in `greeting(name);` is an argument.
**NOTE!** you have to specify the datatype of the parameters.

## return
- it returns a value back to a calling function
- you need to define what datatype will you return when invoking a function
- a void function will not return anything hence the name void

```c
int doubler(int num){
    return num * 2;
}
int main(){
    int result = doubler(69);
    printf("%i", result);
}
```

## function prototype
- function declaration, without a body, before `main()`
- enable to invoke a function after the main function
- ensures that calls to a function are made with the correct arguments
- if a function gets called with less numbers of arguments then its paramer, it will throw an error instead of compiling and running with a wrong output.

```c
int doubler(int num); //function prototype

int main(){
    int result = doubler(69);
    printf("%i", result);
}

int doubler(int num){
    return num * 2;
}
```



