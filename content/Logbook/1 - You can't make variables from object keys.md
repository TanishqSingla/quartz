  
20th October 2021, Wednesday

## About the Day

Today I was assigned to my first task for smallboard, I had to add a filter according to the GrowthUser selected, I did not complete the task today as there is some problem regarding the api (this is my supposition) so I left it to Kavinder Panwar (whom I am discussing about the api,  and he's works in the backend), the request part seems to work as I am sending the api request correctly, the problem is coming when getting the list of growthMembers, well I can do nothing about it as of today.

## In The Night

So I was reading this book called `97 Things Every Programmer should Know` and there was a suggestion about having few number of parameters, and after that I got my eyes stuck on the `getLeadGenUsers` function that had a bunch of parameters, 9 to be precise, I thought it would be cool if instead of destructuring the `state` of the component for getting the values of parameter I use some kind of map functions in JS and using functions fill in those value instead of manually typing all the parameters.

Well, long story short, this was stupid as it can never work. The reasons I am listing below

- Instead of simplifying the complexity of code would be increased.
    - This can be achieved using a `Object.values` and inside of it `Object.entries` and filtering the values with `.filter` .
- To make this work the state would have to be in order and this would make the code more rigid, and it will also require constant monitoring of the object.

## Conclusion

Well this was a stupid idea, when working with JS object don't use too much brain on trivial things such as function parameters. But in the end I got to learn the about `Object.values` `Object.entries` `Object.fromEntries` and got a sense how to work with objects  in JS.

`Object.value` - gets values of keys in objects and stores them in an array

`Object.entries` - stores the values in a object in [key, value] (I consider it as a tuple)

`Object.fromEntries` - Forms an object from [key, value] tuple.

### UPDATE (21st October 2021)

So after having a call with Kavinder he told me not to pass all, which I already fixed, but did not commit, apparently the code was fine but it didn't seem to work that day, however it was working fine when I relaunched it.