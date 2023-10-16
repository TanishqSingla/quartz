27th December 2021, Monday

## Context

Whenever I used typescript in react to make a component I used to declare the component like this.

```js
const GreetingsPage: React.FC<greetingProps> = (props) => { 
	return <div></div> 
}
```

This code is worse than what a newbie what do

## Lesson Learned

Instead of declaring the component type and props like this the types can be inferred in typescript. The example mentioned below is a more elegant choice.

```js
function GreetingsPage(props: greetingProps) {
	return <div></div>
}
```