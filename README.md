# Dictionaries lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

- Create an instance of a dictionary called `citiesDict` that maps 3 countries to their capital cities.

- Add two more countries to your dictionary.

- Translate at least 3 of the capital names into another language.

var citiesDict: [String:String] = ["United States":"Washington D.C", "Canada":"Ottawa", "Mexico":"Mexico City"]

citiesDict["Colombia"] = "Bogata"
citiesDict["Venezuela"] = "Caracas"
citiesDict["Mexico"] = "Ciudad de México"
citiesDict["United States"] = "Waszyngton"
citiesDict["Canada"] = "ਓਟਵਾ"


## Question 2

`var someDict:[String:Int] = ["One": 1, "Two": 4, "Three": 9, "Four": 16, "Five": 25]`

- Using `someDict`, add together the values associated with "Three" and "Five" and print the result.

var someDict:[String:Int] = ["One": 1, "Two": 4, "Three": 9, "Four": 16, "Five": 25]
var three = someDict["Three"]
var five = someDict["Five"]
print(three! + five!)

- Add values to the dictionary for the keys "Six" and "Seven".

someDict["Six"] = 20
someDict["Seven"] = 26

- Make a key called `productUpToSeven` and set its value equal to the product of all the values.

var two = 1
for (_,value) in someDict {
two = value * two
}
someDict["productUpToSeven"] = two

print(someDict["productUpToSeven"])

- Make a key called `sumUpToSix` and set its value equal to the sum of the keys "One", "Two", "Three", "Four", "Five" and "Six".

var someDict:[String:Int] = ["One": 1, "Two": 4, "Three": 9, "Four": 16, "Five": 25]
var three = someDict["Three"]
var five = someDict["Five"]
print(three! + five!)

someDict["Six"] = 20
someDict["Seven"] = 26
var one = 0
for (_,value) in someDict where value != 26 {
one += value
}
someDict["SumUpToSix"] = one

print(someDict["SumUpToSix"]!)

- Remove the new keys made in the previous two steps

- Add 2 to every value inside of `someDict`.

var newDict = someDict
for (key,value) in someDict {
newDict[key] = value + 2
}
print(newDict)


## Question 3

Create a variable that is explicitly typed as a dictionary that maps strings to floating point numbers. Initialize the variable to the data shown in the table below which lists an author name and their comprehensibility score.

| Author Name |	Score |
| :--: | :--: |
| Mark Twain |	8.9 |
| Nathaniel Hawthorne	| 5.1 |
| John Steinbeck	| 2.3 |
| C.S. Lewis | 9.9 |
| Jon Krakauer | 6.1 |

Using the dictionary created in the previous problem, do the following:

- Print out the floating-point score for “John Steinbeck”.

Dictionary = ["Mark Twain":8.9,"Nathaniel Hawthorne":5.1,"John Steinbeck":2.3,"C.S Lewis":9.9,"Jon Krakauer":6.1]
print(Dictionary["John Steinbeck"]!)
Dictionary["Erik Larson"] = 9.2

- Add an additional author named “Erik Larson” with an assigned score of 9.2.



- Write an if/else statement that compares the score of John Krakaur with Mark Twain. Print out the name of the author with the highest score.

if Dictionary["Mark Twain"]! > Dictionary["John Steinbeck"]! {
print("Mark Twain")
} else {
print("John Steinbeck")
}


- Use a for-loop to iterate through the dictionary you created at the beginning of the problem, and print out the content in the form of key: value, one entry per line.

var Dictionary: [String:Double]
Dictionary = ["Mark Twain":8.9,"Nathaniel Hawthorne":5.1,"John Steinbeck":2.3,"C.S Lewis":9.9,"Jon Krakauer":6.1]

for (key,value) in Dictionary {
print("\(key): \(value)")
}


## Question 4

You are given a dictionary code of type [String:String] which has values for all lowercase letters. The code dictionary represents a way to encode a message. For example if code["a"] = "z" and code["b"] = "x" the encoded version if "ababa" will be "zxzxz". You are also given a message which contains only lowercase letters and spaces. Use the `code` dictionary below to encode the message and print it.

```swift
var code = [
    "a" : "b",
    "b" : "c",
    "c" : "d",
    "d" : "e",
    "e" : "f",
    "f" : "g",
    "g" : "h",
    "h" : "i",
    "i" : "j",
    "j" : "k",
    "k" : "l",
    "l" : "m",
    "m" : "n",
    "n" : "o",
    "o" : "p",
    "p" : "q",
    "q" : "r",
    "r" : "s",
    "s" : "t",
    "t" : "u",
    "u" : "v",
    "v" : "w",
    "w" : "x",
    "x" : "y",
    "y" : "z",
    "z" : "a"
]

var message = "hello world"
```
var message = "hello world"

var empty2 = ""
for letter in message {
code[String(letter)] = code[String(letter)] ?? " "
empty2 += code[String(letter)]!
}
print(empty2)


You are also given an `encodedMessage` which contains only lowercase letters and spaces. Use the `code` dictionary to decode the message and print it.
`var encodedMessage = "uijt nfttbhf jt ibse up sfbe"`

var encodedMessage = "uijt nfttbhf jt ibse up sfbe"


for letter in encodedMessage {
code[String(letter)] = code[String(letter)] ?? " "
empty2 += code[String(letter)]!
}

print(empty2)


## Question 5

You are given an array of dictionaries. Each dictionary in the array contains exactly 2 keys `“firstName”` and `“lastName”`. Create an array of strings called `firstNames` that contains only the values for `“firstName”` from each dictionary.


var firstName = [String]()
for names in people {
for (key,value) in names where key == "firstName" {
firstName += [value]
}
}
print(firstName)

```swift
var people: [[String:String]] = [
    [
        "firstName": "Calvin",
        "lastName": "Newton"
    ],
    [
        "firstName": "Garry",
        "lastName": "Mckenzie"
    ],
    [
        "firstName": "Leah",
        "lastName": "Rivera"
    ],
    [
        "firstName": "Sonja",
        "lastName": "Moreno"
    ],
    [
        "firstName": "Noel",
        "lastName": "Bowen"
    ]
]
```

Now, create an array of strings called `fullNames` that contains the values for `“firstName”` and `“lastName”` from the dictionary separated by a space.

var fullName = [String]()
for people1 in people {
if let firstName2 = people1["firstName"] {
if let lastName2 = people1["lastName"] {
fullName += [("\(firstName2) \(lastName2)")]
}

}
}
print(fullName)


## Question 6

You are given an array of dictionaries. Each dictionary in the array describes the score of a person. Find the person with the best score and print his full name.

var bestScore = 0
var fullname = ""
for people in peopleWithScores {
if let bestScore1 = people["score"] {
if let firstName1 = people["firstName"] {
if let lastName1 = people["lastName"] {
if Int(bestScore1)! > bestScore {
bestScore = Int(bestScore1)!
fullname = ("\(firstName1) \(lastName1)")
}
}
}
}
}
print("\(fullname)'s score is \(bestScore)")

```swift
var peopleWithScores: [[String: String]] = [
    [
        "firstName": "Calvin",
        "lastName": "Newton",
        "score": "13"
    ],
    [
        "firstName": "Garry",
        "lastName": "Mckenzie",
        "score": "23"
    ],
    [
        "firstName": "Leah",
        "lastName": "Rivera",
        "score": "10"
    ],
    [
        "firstName": "Sonja",
        "lastName": "Moreno",
        "score": "3"
    ],
    [
        "firstName": "Noel",
        "lastName": "Bowen",
        "score": "16"
    ]
]
```

Print out the dictionary above in the following format:  **full name - score**

var fullname = ""
for people in peopleWithScores {
if let people1 = people["firstName"] {
if let people2 = people["score"] {
print("\(people1) score \(people2)")
}
}
}

## Question 7

`var numbers = [1, 2, 3, 2, 3, 5, 2, 1, 3, 4, 2, 2, 2]`

You are given an array of integers. The frequency of a number is the number of times it appears in the array. Find out the frequency of each one.

Print the numbers in ascending order followed by their frequency.

var count1 = ""
var count2 = ""
var count3 = ""
var count4 = ""
var count5 = ""
for freq in numbers {
if freq == 1 {
count1 += String(freq)
}
if freq == 2 {
count2 += String(freq)
}
if freq == 3 {
count3 += String(freq)
}
if freq == 4 {
count4 += String(freq)
}
if freq == 5 {
count5 += String(freq)

}
}
print("In Array \(numbers.sorted()) 1 appears \(count1.count) times, 2 appears \(count2.count) times, 3 appears \(count3.count) times, 4 appears \(count4.count) times and 5 appears \(count5.count) times.")

## Question 8

Print the most common letter in the string below:

`var myString = "We're flooding people with information. We need to feed it through a processor. A human must turn information into intelligence or knowledge. We've tended to forget that no computer will ever ask a new question."`

var a = ""
var b = ""
var c = ""
var d = ""
var e = ""
var f = ""
var g = ""
var h = ""
var i = ""
var j = ""
var k = ""
var l = ""
var m = ""
var n = ""
var o = ""
var p = ""
var q = ""
var r = ""
var s = ""
var t = ""
var u = ""
var v = ""
var w = ""
var x = ""
var y = ""
var z = ""
var MostCommonNumber = 0
var MostCommon = ""
for char in myString.lowercased() {
if char == "a" {
a += String(char)
if a.count > MostCommonNumber {
MostCommonNumber = a.count
MostCommon = "a"
}

}
if char == "b" {
b += String(char)
if b.count > MostCommonNumber {
MostCommonNumber = b.count

MostCommon = "b"
}
}
if char == "c" {
c += String(char)
if c.count > MostCommonNumber {
MostCommonNumber = c.count

MostCommon = "c"
}
}
if char == "d" {
d += String(char)
if d.count > MostCommonNumber {
MostCommonNumber = d.count

MostCommon = "d"
}
}
if char == "e" {
e += String(char)
if e.count > MostCommonNumber {
MostCommonNumber = e.count

MostCommon = "e"
}
}
if char == "f" {
f += String(char)
if f.count > MostCommonNumber {
MostCommonNumber = f.count

MostCommon = "f"
}
}
if char == "g" {
g += String(char)
if g.count > MostCommonNumber {
MostCommonNumber = g.count

MostCommon = "g"
}
}
if char == "h" {
h += String(char)
if h.count > MostCommonNumber {
MostCommonNumber = h.count

MostCommon = "h"
}
}
if char == "i" {
i += String(char)
if i.count > MostCommonNumber {
MostCommonNumber = i.count

MostCommon = "i"
}
}
if char == "j" {
j += String(char)
if j.count > MostCommonNumber {
MostCommonNumber = j.count

MostCommon = "j"
}
}
if char == "k" {
k += String(char)
if k.count > MostCommonNumber {
MostCommonNumber = k.count

MostCommon = "k"
}
}
if char == "l" {
l += String(char)
if a.count > MostCommonNumber {
MostCommonNumber = l.count

MostCommon = "l"
}
}
if char == "m" {
m += String(char)
if m.count > MostCommonNumber {
MostCommonNumber = m.count

MostCommon = "m"
}
}
if char == "n" {
n += String(char)
if n.count > MostCommonNumber {
MostCommonNumber = n.count

MostCommon = "n"
}
}
if char == "o" {
o += String(char)
if o.count > MostCommonNumber {
MostCommonNumber = o.count

MostCommon = "o"
}
}
if char == "p" {
p += String(char)
if p.count > MostCommonNumber {
MostCommonNumber = p.count

MostCommon = "p"
}
}
if char == "q" {
q += String(char)
if q.count > MostCommonNumber {
MostCommonNumber = q.count

MostCommon = "q"
}
}
if char == "r" {
r += String(char)
if r.count > MostCommonNumber {
MostCommonNumber = r.count

MostCommon = "r"
}
}
if char == "s" {
s += String(char)
if s.count > MostCommonNumber {
MostCommonNumber = s.count

MostCommon = "s"
}
}
if char == "t" {
t += String(char)
if t.count > MostCommonNumber {
MostCommonNumber = t.count

MostCommon = "t"
}
}
if char == "u" {

u += String(char)
if u.count > MostCommonNumber {
MostCommonNumber = u.count

MostCommon = "u"
}
}
if char == "v" {
v += String(char)
if v.count > MostCommonNumber {
MostCommonNumber = v.count

MostCommon = "v"
}
}
if char == "w" {
w += String(char)
if w.count > MostCommonNumber {
MostCommonNumber = w.count

MostCommon = "w"
}
}
if char == "x" {
x += String(char)
if x.count > MostCommonNumber {
MostCommonNumber == x.count

MostCommon = "x"
}
}
if char == "y" {
y += String(char)
if y.count > MostCommonNumber {
MostCommonNumber = y.count

MostCommon = "y"
}
}
if char == "z" {
z += String(char)
if z.count > MostCommonNumber {
MostCommonNumber = z.count

MostCommon = "z"
}
}

}
print("\(MostCommon) is the most common letter")




## Question 9

Write code that creates a dictionary where the keys are Ints between 0 and 20 inclusive, and each key's value is its cube.


## Question 10

Write code that iterates through `testStates` and prints out whether or not that key is in `statePop`.



```swift
let statePop = ["Alabama": 4.8, "Alaska": 0.7, "Arizona": 6.7, "Arkansas": 3.0]
let testStates = ["California","Arizona", "Alabama", "New Mexico"]
```
let statePop = ["Alabama": 4.8, "Alaska": 0.7, "Arizona": 6.7, "Arkansas": 3.0]
let testStates = ["California","Arizona", "Alabama", "New Mexico"]
var InStatePop = ""
for states in testStates {
for (key,_) in statePop {
if key == states {
InStatePop += states + " "


}
}
}

print("These states are in StatePop - \(InStatePop)")

## Question 11

You are given the dictionary `deposits`, which maps a persons name to an array of deposits that have been made to their account.

a) Write code to to print the name and total amount deposited of the person who recieved the most money.

b) Create an array called `stolenCents`, iterate over deposits for each person and steal their cents! ... like Office Space or Superman 3. Calculate the decimal part of each value, add it to the `stolenCents` array and round down the value in the dict.

c) How much money did you steal?

```swift
var deposits: [String: [Double]] = [
 "Williams" : [300.65, 270.45, 24.70, 52.00, 99.99],
 "Cooper" : [200.56, 55.00, 600.78, 305.15, 410.76, 35.00],
 "Davies" : [400.98, 56.98, 300.00],
 "Clark" : [555.23, 45.67, 99.95, 80.76, 56.99, 46.50, 265.70],
 "Johnson" : [12.56, 300.00, 640.50, 255.60, 26.88]
]
```


## Question 12

Print the second most common letter in the string below:

`var myString = "We're flooding people with information. We need to feed it through a processor. A human must turn information into intelligence or knowledge. We've tended to forget that no computer will ever ask a new question."`


## Question 13

Given the below 4 arrays of Ints,

a) create a new array, sorted in ascending order, that contains all the values without duplicates.

let arr1 = [2, 4, 5, 6, 8, 10, 12]
let arr2 = [1, 2, 3, 4, 5, 6]
let arr3 = [5, 6, 7, 8, 9, 10, 11, 12]
let arr4 = [1, 3, 4, 5, 6, 7, 9]
var newArr: [Int] = []
for num in arr1 where newArr.contains(num) != true {
newArr.append(num)
}
for num1 in arr2 where newArr.contains(num1) != true {
newArr.append(num1)
}
for num2 in arr3 where newArr.contains(num2) != true {
newArr.append(num2)
}
for num3 in arr4 where newArr.contains(num3) != true {
newArr.append(num3)
}




print(newArr.sorted())


b) create another new array that contains unique values that appear in all 4 arrays.

```swift
let arr1 = [2, 4, 5, 6, 8, 10, 12]
let arr2 = [1, 2, 3, 4, 5, 6]
let arr3 = [5, 6, 7, 8, 9, 10, 11, 12]
let arr4 = [1, 3, 4, 5, 6, 7, 9]
```


## Question 14

Given the following exert from the Declaration of Independence, find the most frequent word that is longer than 5 characters.

 - use `components(separatedBy:)` to break up the string into an array.

 - use `CharacterSet.punctuationCharacters` in union with any other characters you don't want in your array, like spaces and new lines.

 ```swift
let declarationOfIndependence = """
When in the Course of human events, it becomes necessary for one people to dissolve the
political bands which have connected them with another, and to assume among the powers of the
earth, the separate and equal station to which the Laws of Nature and of Nature's God entitle
them, a decent respect to the opinions of mankind requires that they should declare the causes
which impel them to the separation.

We hold these truths to be self-evident, that all men are created equal, that they are endowed by
their Creator with certain unalienable Rights, that among these are Life, Liberty and the pursuit
of Happiness. That to secure these rights, Governments are instituted among Men, deriving
their just powers from the consent of the governed, That whenever any Form of Government
becomes destructive of these ends, it is the Right of the People to alter or to abolish it, and to
institute new Government, laying its foundation on such principles and organizing its powers in
such form, as to them shall seem most likely to effect their Safety and Happiness. Prudence,
indeed, will dictate that Governments long established should not be changed for light and
transient causes; and accordingly all experience hath shewn, that mankind are more disposed to
suffer, while evils are sufferable, than to right themselves by abolishing the forms to which they
are accustomed. But when a long train of abuses and usurpations, pursuing invariably the same
Object evinces a design to reduce them under absolute Despotism, it is their right, it is their duty,
to throw off such Government, and to provide new Guards for their future security. Such has
been the patient sufferance of these Colonies; and such is now the necessity which constrains
them to alter their former Systems of Government. The history of the present King of Great
Britain is a history of repeated injuries and usurpations, all having in direct object the
establishment of an absolute Tyranny over these States. To prove this, let Facts be submitted to a
candid world.
"""
```
