<hr>
#computerscience  #infix 
# Infix Expressions:
- In infix expressions, the operators are placed between the operands. This is the term generally used in everyday mathematics. 2 + 3 is an example of infix expression.
- Parenthesis are used in infix notation to specify the order of the operation, i.e. (2 + 3) * 5 shows that the sum is to be calculated first and then the product is to be operated on the result.
#### Operator precedence in infix:
- Parenthesis -> Exponents -> Multiplication and Division -> Addition and Subtraction .
#### Evaluating infix expression:
It requires additional processing to handle the precedence of the parenthesis and operators according to their precedence. This can be done using a stack or a recursive algorithm. Then it can be used to evaluate a post-fix expression.

| Advantages                                                                      | Disadvantages                                               |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Natural to the reader, and <br>easy to understand.                              | Requires parenthesis to specify <br>the order of operation. |
| Widely used and supported by<br>most programming languages and <br>calculators. | Can be difficult to parse and<br>evaluate efficiently.      |
<hr>
# Prefix Expression (Polish Notation): 
#prefix
In this mathematical notation, the operator precedes the operands. +ab is an example of Polish notation which can be translated to a + b.
#### Evaluating Prefix expressions:
Evaluating prefix expressions can be useful in certain scenarios, such as when dealing with expressions that have a large number of nested parentheses or when using a stack-based programming language.

#### Conversion of Infix to Prefix Steps + Code:

- Place a pointer at the end of the string and loop till index 0, decrementing the pointer by one index at each step.
- In the loop body select the current character and check whether it is a operator or operand.
- If it is an **operand** push it into the stack
- Else, in case of an **operator** pop the two elements of the stack which are bound to be previously inserted operands.
- End of loop body.
- Return the top element of the stack that now stores the evaluated prefix expression.

```C++

bool isOperand(char ch){
	return isdigit(ch);
}

double evaluatePrefix(string expression){
	stack<double> st;
	for(int i = expression.size()-1; i >= 0; i--){
		char temp = expression[j];
		if(isOperand(temp)){
			st.push(temp);
		}else{
			double o1 = st.top();
			st.pop();
			double o2 = st.top();
			st.pop();
			// Operate on the operators
			if(temp == '+'){
				//add the elements and push to stack
			}else if(temp == '-') // subtract the elements and push to stack
			else if(temp == '*') // multiply and push to stack
			else{
				// divide and push to stack
			}
		}
	}
	return stack.top();
}
```


| Advantages                                                                                         | Disadvantages                                                                |
| -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| No parenthesis needed, confusion is<br>avoided for larger expressions with <br>nested parenthesis. | While it is easy to evaluate , it is <br>difficult for human interpretation. |
| Easier to parse using a stack based <br>algorithm.                                                 | Not as Commonly used as infix <br>notations.                                 |
<hr>

# Postfix Expression (Reverse Polish):
#postfix
Also known as the reverse polish notation, postfix expression is the exact opposite of the polish expression, where the operator follows the operands. The infix notation 1 + 2 can be translated to 1 2 + as postfix notation.

#### Evaluating Postfix expressions:
Evaluating postfix expressions can be useful in certain scenarios, such as when dealing with expressions that have a large number of nested parentheses or when using a stack-based programming language.

#### Conversion of Postfix to Infix:
- Start from the beginning of the expression and iterate till the end.
- If the expression is an operand push it to stack.
- Upon encountering an operator pop the last to elements, evaluate the respective value and push it to the stack.
- End of loop, the top element of the stack will have the evaluated postfix expression stored in itself.

```C++
bool isOperand(char ch){
	return isdigit(ch);
}

double evaluatePrefix(string expression){
	stack<double> st;
	for(int i = 0; i < expression.size; i++){
		char temp = expression[j];
		if(isOperand(temp)){
			st.push(temp);
		}else{
			double o1 = st.top();
			st.pop();
			double o2 = st.top();
			st.pop();
			// Operate on the operators
			if(temp == '+'){
				//add the elements and push to stack
			}else if(temp == '-') // subtract the elements and push to stack
			else if(temp == '*') // multiply and push to stack
			else{
				// divide and push to stack
			}
		}
	}
	return stack.top();
}
// This is basically the same code as prefix evaluation but the order of 
// traversal is reversed.
```

<hr>

- Link for further reading [GFG](https://www.geeksforgeeks.org/infix-postfix-prefix-notation/#infix-expressions)
<hr>

## Practice Questions on The Topic:
