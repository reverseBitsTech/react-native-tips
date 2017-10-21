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

when you wants to use lifecycle methods and and do complex things with states, prefer class level components as they are more powerful.

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



### De structuring of objects

#### At component level

Whenever you want to fetch multiple things from a JS object like you have multiple styles defined inside styles object:

```jsx
const styles = {

    viewStyle: {

        backgroundColor: '#F8F8F8',

        justifyContent: 'center',

        alignItems: 'center',

        elevation: 8,

        position: 'relative'

    },

    textStyle: {

        fontSize: 20

    }

}
```

And now you want to access these both at some place, then use de structuring of objects so instead of writing like this :

```
<View style={this.styles.viewStyle}>

     <Text style={this.styles.textStyle}> {props.headerText} </Text>

</View>
```

1. First make a different constant

   ```
   const { textStyle, viewStyle } = styles;
   ```

2. Use it directly this way, 

   ```
   <View style={viewStyle}>

       <Text style={textStyle}> {props.headerText} </Text>

   </View>
   ```

This makes code lot more readable and clean ;)



