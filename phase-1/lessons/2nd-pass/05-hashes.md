# Hashes

```
kids =
  brother:
    name: "Max"
    age:  11
  sister:
    name: "Ida"
    age:  9

kids['brother']
kids.brother
kids.brother.name


```

## JavaScript Hash

```
var john = {firstName: 'John', lastName: 'Smith'}
john.firstName
#John

john.lastName
#Smith

var jane = {firstname: "Jane:"}

#show an object's class
jane..__proto__
>Object

#jane and john
jane.__proto__ = john
jane
> Object {firstName: "Jane", firstName: "John", lastName: "Smith" }

jane.lastName = "Doe"

jane
> Object {firstName: "Jane", firstName: "John", lastName: "Smith", lastName: "Doe" }


delete jane.firstName
> Object {firstName: "John", lastName: "Smith", lastName: "Doe" }
```

## Resources

- [Arrays & Hashes](https://gist.github.com/mddub/6184b707d52ca6f66eff)

