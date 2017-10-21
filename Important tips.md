# Important Lessons learned while learning React Native



### Uses of components: functional, class components

#### Functional components 

When you **just wants to return some JSX** from a component then use functional level component

Example:

```jsx
const Button = () => {	

     return(

        <View> click me </View>

     );

}
```

Like here we don't perform any operation other than returning a View.

#### Class level components

when you **wants to use lifecycle methods and and do complex things** with states, prefer class level components as they are more powerful.

```jsx
class Button extends Component {

 		 // A react lifecycle method...
  		 componentWillMount() {
       		//Here do something relative...
   		 }
  
        render() {

        return (

            <View>

                <Text>

                </Text>

            </View>

        );

    }

}
```





