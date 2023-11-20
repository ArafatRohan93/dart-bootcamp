# OOP in Dart

By Shadman Sakib

ডার্ট একটি অবজেক্ট ওরিয়েন্টেড পোগ্রামিং ভাষা। ডার্ট বুটকাম্প এর এই অধ্যায়ে আমরা খুঁজে বের করার চেষ্টা করব কিভাবে ডার্ট এ
অবজেক্ট ওরিয়েন্টেড পোগ্রামিং এর বৈশিষ্ট্য গুলোকে প্রয়োগ করা হয়েছে ।

## ক্লাস এবং অবজেক্ট

অবজেক্ট ওরিয়েন্টেড পোগ্রামিং নিয়ে কথা বলতে গেলে শুরুতেই যে জিনিসটি সামনে চলে আসে সেটি হল ক্লাস এবং অবজেক্ট। আমরা প্রথমে
আলোচনা শুরু করব ক্লাস নিয়ে এবং পরবর্তীতে চলে যাব অবজেক্ট এর কাছে।

ক্লাস হচ্ছে অবজেক্ট এর একটি ব্লুপ্রিন্ট বা নকশা।এর অর্থ হচ্ছে একটি অবজেক্ট কি কি বৈশিষ্ট্য ধারণ করতে পারে, কি কি কাজ
করতে পারে তা ডিফাইন করা থাকে একটা ক্লাসের ভেতরে, অপরদিকে অবজেক্ট হচ্ছে সেই ক্লাসের একটি উপাদান বা ইন্সট্যান্স যা মূলত
ক্লাস থেকে সৃষ্ট সমস্ত বৈশিষ্ট্য ধারণ করে। একটা উদাহরন দেওয়া যাক।আমরা একটা গাড়ির কথা চিন্তা করি, একটা গাড়ির কি থাকে?
চাকা থাকে, সিট থাকে, তেলের ট্যাংক থাকে ইত্যাদি ইত্যাদি। এখন আমরা যদি গাড়ির একটা সফটওয়ার বানাতে চাই তাহলে আমাদের কি
লাগবে? আমাদের চাকার সাইজ আমাদের একটা ভ্যারিয়েবলে রাখতে হবে, সিটের সংখ্যার জন্য ভ্যারিয়েবল লাগবে, তেলের ট্যাঙ্কের জন্য
ভ্যারিয়েবল লাগবে ইত্যাদি ইত্যাদি। এ ছাড়া গাড়ির বিভিন্ন ফাংশন গুলোর জন্য অনেক গুলো ফাংশন আমাদের লিখতে হবে।এখন আমরা এই
সমস্যাটি সমাধান করার জন্য একটি ক্লাস বানাব, ক্লাসটি হবে একটি গাড়ির ব্লুপ্রিন্ট এবং ক্লাসটি লিখব আমরা ডার্ট ল্যাঙ্গুয়েজ
এ।

``` Java
class Car {
String manufacturerCompany = 'BMW';
String color = 'Black';
int numberOfSeats = 4;
}
```

ডার্ট ল্যাঙ্গুয়েজ এ ক্লাস তৈরি করার জন্যে class কিওয়ার্ড টি ব্যাবহার করতে হয়।আমরা খুবই সাধারণ একটি Car ক্লাস তৈরি করলাম
যেখানে ক্লাস ভারিয়েবল হিসেবে রাখা হয়েছে গাড়ি তৈরির কোম্পানির নাম,গাড়িটির রঙ কি হবে সেটা এবং গাড়িটিতে কয়টি সিট থাকবে।
তাহলে আমাদের ক্লাস তৈরি হয়ে গেল, এখন আমরা চলে যাব অবজেক্ট নিয়ে কথা বলতে ।

একদম সহজ কথায় এই কার ক্লাসটির ব্লুপ্রিন্ট/নকশা ব্যাবহার করে আমরা যে গাড়িটি তৈরি করব সেটিই হবে একটা অবজেক্ট, আমাদের Car
ক্লাসটির একটা অবজেক্ট।তাহলে আমরা ডার্ট ল্যাঙ্গুয়েজ ব্যাবহার করে Car ক্লাসের একটা অবজেক্ট তৈরি করে ফেলি

```Java
class Car {
String manufacturerCompany = 'BMW';
String color = 'Black';
int numberOfSeats = 4;
}

void main() {
Car car = Car();
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

আউটপুট:

```
BMW
Black
4
```

এখানে `Car` ক্লাস এর একটা অবজেক্ট তৈরি হল, যার নাম দেওয়া হয়েছে `car` এবং এই অবজেক্ট টিকে ব্যাবহার করে আমরা কনসোলে `Car`
ক্লাসটির বিভিন্ন ভ্যারিয়েবল গুলোকে প্রিন্ট করে দেখলাম।

## কনস্ট্রাকটর:

কন্সট্রাক্টর হল ক্লাসের একটি মেথড । যখন আমরা কোন একটি ক্লাসের অবজেক্ট তৈরি করতে যাই তখন ক্লাসের কন্সট্রাক্টর মেথড কল হয়ে
এবং অব্জেক্টিকে তৈরি করে দেয় । কন্সট্রাক্টরের নাম এবং ক্লাস এর নাম একই থাকে ।

## ডিফল্ট কন্সট্রাক্টরঃ

একটু আগেই আমরা Car ক্লাসের একটি অবজেক্ট তৈরি করেছি । এখন প্রশ্ন হল Car ক্লাসের কন্সট্রাক্টরটি তাহলে কোথায় ? আমরা যদি কোন
ক্লাসের কোন কন্সট্রাক্টর মেথড কে ডিফাইন না করে দেই তাহলে ক্লাসটি নিজেই তার একটি কন্সট্রাক্টর তৈরি করে নিয়ে অবজেক্ট তৈরি
অথবা ইনিশিয়ালাইযেশন এর কাজটি করে ফেলে।

```Java
class Car {
String manufacturerCompany = 'BMW';
String color = 'Black';
int numberOfSeats = 4;

// Default Constructor
Car();
}

void main() {
Car car = Car();
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

## কন্সট্রাক্টর উইথ প্যারামিটারসঃ

আমাদের Car ক্লাসের ভেরিয়েবল গুলোকে আমরা স্ট্যাটিক ভ্যালু দিয়ে রেখেছি । আমরা যদি চাই , এভাবে স্ট্যাটিক ভ্যালু না দিয়ে
অবজেক্ট তৈরি করার সময়ে আমরা আমাদের সুবিধা মতন ভ্যালু দিয়ে অবজেক্টটি তৈরি করব, তাহলে আমরা আমাদের কন্সট্রাক্টর মেথডটিতে
প্যারামিটার পাস করে দিতে পারি । নিচের কোড এক্সাম্পলটি দেখলেই বিষয়টি আমরা বুঝতে পারব।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany,
this.color,
this.numberOfSeats,
);
}

void main() {
Car car = Car('Toyota', 'Green', 4);
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

আউটপুট:

```Java 
Toyota
Green
4
```

আমরা জানি যে ডার্ট ল্যাঙ্গুয়েজ নেমড প্যারামিটার এর সুবিধা দিয়ে থাকে । আমরা এখন আমাদের কন্সট্রাক্টর এ পাস করা প্যারামিটার
গুলোকে নেমড প্যারামিটার দিয়ে ইমপ্লিমেন্ট করে দেখব

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car({
required this.manufacturerCompany,
required this.color,
required this.numberOfSeats,
});
}

void main() {
Car car = Car(
manufacturerCompany: 'Toyota',
color: 'Green',
numberOfSeats: 4,
);
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

আউটপুট :

```Java 
Toyota
Green
4
```

নেমড প্যারামিটার ব্যাবহার করার কিছু সুবিধা হল, যেমন : প্যারামিটার গুলো কি কাজ করতেছে সেটার একটা ভালো ব্যাখ্যা পাওয়া যায়
এবং প্যারামিটার গুলোর সিরিয়ালটিকে মনে রাখার প্রয়োজন পরে না।

এখন এখানে একটা প্রশ্ন আসতে পারে যে একটা গাড়ির তো সাধারণত চারটি সিট হয়ে থাকে, তাহলে আমরা বারবার প্যারামিটার এ ভ্যালু পাস
না করে যখন দরকার তখনই কেবল পাস করতে চাই । এই কাজটাও আমরা করতে পারই আমাদের নেমড প্যারামিটার এ কোন একটা ডিফল্ট ভ্যালু সেট
করে দিয়ে। নিচের কোড এক্সাম্পলটি দেখে নেই ।

```Java 
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car({
required this.manufacturerCompany,
required this.color,
this.numberOfSeats = 4,
});
}

void main() {
Car car = Car(
manufacturerCompany: 'Toyota',
color: 'Green',
);
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

আউটপুট :

```Java
Toyota
Green
4
```

এখন এই কন্সট্রাক্টর এ যদি `numberOfSeats` এর কোন ভ্যালু পাস করি তাহলে ওই ভ্যালু দিয়ে অবজেক্ট তৈরি হবে আর পাস না করলে
ডিফল্ট ভ্যালু 4 দিয়েই অবজেক্ট তৈরি হবে ।

ডার্ট ল্যাঙ্গুয়েজ তার কোন একটি ক্লাসের কন্সট্রাক্টর এ অপশনাল পজিশনাল প্যারামিটার এর সুবিধাও দিয়ে থাকে । থার্ড ব্রাকেট এর
মধ্যে যে প্যারামিটার গুলোকে ডিফাইন করে দেওয়া আছে সেগুলোই হল অপশনাল প্যারামিটার। আমরা এই বিষয়ের একটি কোড এক্সাম্পল দেখে
কন্সট্রাক্টর উইথ প্যারামিটারস নিয়ে আলোচনার ইতি টানব ।

```Java 
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany, [
this.color = 'Green',
this.numberOfSeats = 4,
]);
}

void main() {
Car car = Car(
'Toyota',
);
print(car.manufacturerCompany);
print(car.color);
print(car.numberOfSeats);
}
```

আউটপুট :

```Java 
Toyota
Green
4
```

## নেমড কন্সট্রাক্টরঃ

অন্যান্য কিছু অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং ল্যাঙ্গুয়েজ এ কন্সট্রাক্টর ওভেরলোড er সুবিধা দেওয়া থাকলেও ডার্টে এই
সুবিধাটা পাওয়া যায় না । এর মানে হল কোন একটি ক্লাস এ একই নামের দুই বা তার বেশি কন্সট্রাক্টর মেথড ডিফাইন করা যায় না ।
কিন্তু ডার্ট এই সমস্যাটির খুব সহজ এবং সুন্দর একটি সমাধান দিয়েছে , আর সেটি হল নেমড কন্সট্রাক্টর ব্যাবহার করা। নেমড
কন্সট্রাক্টর ব্যাবহার করে আমরা একটি ক্লাসে যেমন অনেকগুলো কন্সট্রাক্টর রাখতে পারি , ঠিক একই সাথে কোন কন্সট্রাক্টরটি কি
কাজে ব্যাবহার করা হচ্ছে সেটার ও একটি সুন্দর ধারণা পাওয়া যায় ।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany, [
this.color = 'Black',
this.numberOfSeats = 4,
]);

Car.madeByBmw({
this.manufacturerCompany = 'BMW',
required this.color,
required this.numberOfSeats,
});

Car.madeByToyota({
this.manufacturerCompany = 'Toyota',
required this.color,
required this.numberOfSeats,
});
}

void main() {
Car bmwCar = Car.madeByBmw(
color: 'Black',
numberOfSeats: 4,
);

Car toyotaCar = Car.madeByToyota(
color: 'Green',
numberOfSeats: 6,
);

print(bmwCar.manufacturerCompany);
print(bmwCar.color);
print(bmwCar.numberOfSeats);

print(toyotaCar.manufacturerCompany);
print(toyotaCar.color);
print(toyotaCar.numberOfSeats);

}
```

আউটপুট:

```Java
BMW
Black
4
Toyota
Green
6
```

এখানে প্রথম নেমড কন্সট্রাক্টর দিয়ে BMW টাইপের এবং দ্বিতীয় নেমড কন্সট্রাক্টর দিয়ে Toyota টাইপের গাড়ির অবজেক্ট তৈরি করা
হয়েছে ।

## প্রাইভেট কন্সট্রাক্টরঃ

ডার্টে কোন কন্সট্রাক্টরকে প্রাইভেট কন্সট্রাক্টর হিসিবেও ডিফাইন করে দেওয়া যায়। আমরা যদি চাই আমাদের ক্লাসের কোন অবজেক্ট
বাইরের কেউ অথবা ক্লাসটি যে ব্যাবহার করবে সে তৈরি করতে পারবেনা তখন আমরা কন্সট্রাক্টরকে প্রাইভেট হিসেবে ডিক্লেয়ার করে দিতে
পারি । প্রাইভেট কন্সট্রাক্টর সাধারণত ব্যাবহার করা হয় সিঙ্গেল্টন ক্লাসের ক্ষেত্রে, ফ্যাক্টরি মেথডে, কোন একটা ক্লাসে যদি
শুধুমাত্র স্ট্যাটিক মেথড থাকে তবে এবং কন্সটান্ট ক্লাসের ক্ষেত্রে ।

```Java
class PrivateConstructor {
PrivateConstructor._internal();
}

void main(){
PrivateConstructor privateConstructor = PrivateConstructor();
}
```

এভাবে করে `PrivateConstructor` ক্লাসের কোন অবজেক্ট ডার্ট তৈরি করতে দিবেনা কারণ `PrivateConstructor` ক্লাসের কোন পাবলিক
কন্সট্রাক্টর ডিফাইন করে দেওয়া নাই । এই কোডটি লেখার পরে একটি কম্পাইলার এরর শো করবে ।

## কন্সটান্ট কন্সট্রাক্টরঃ

ডার্ট আমাদেরকে কন্সটান্ট কন্সট্রাক্টর তৈরি করে দেওয়ার সুবিধা দেয় । এটার মানে কি দাঁড়ালো ? আমরা যদি এমন একটা ক্লাস ডিজাইন
করি যার কোন অবজেক্ট একবার তৈরি হওয়ার পরে আর বদলানর কোন সুযোগ নাই তাহলে আমরা সেই ক্লাসটির কন্সট্রাক্টরকে কন্সটান্ট
কন্সট্রাক্টর হিসিবে ডিফাইন করে দিতে পারি । তবে মনে রাখতে হবে এই ক্ষেত্রে ক্লাসের সব ভেরিয়েবল গুলোকে হতে হবে ফাইনাল
ভেরিয়েবল।

```Java
class BlackFourSeaterCarMadeByBMW {
final String manufacturerCompany;
final String color;
final int numberOfSeats;

const BlackFourSeaterCarMadeByBMW(
this.manufacturerCompany,
this.color,
this.numberOfSeats,
);
}
```

## ফ্যাক্টরি কন্সট্রাক্টরঃ

ডার্টে ফ্যাক্টরি কন্সট্রাক্টর ব্যাবহার করতে পারা যায় । তবে ফ্যাক্টরি কন্সট্রাক্টর কি? কেন এবং কোথায় ব্যাবহার করা হয় সেটি
নিয়ে আমরা আবার আলোচনা করব এই অধ্যায়ের শেষে। ডার্ট ল্যাঙ্গুয়েজ এর কন্সট্রাক্টর নিয়ে আলোচনার এখানেই আপাতত ইতি ।

ফ্যাক্টরি কন্সট্রাক্টর এর মাধ্যমেও কোন ক্লাসের অবজেক্ট তৈরি করা যায় কিন্তু এক্ষেত্রে অবজেক্ট তৈরির সময় আমরা কিছু লজিক
চেক করে নিতে পারি। যেমন ধরা যায় আমাদের কোন একটি ক্লাসের অবজেক্ট দিয়ে ডাটাবেস থেকে কিছু ডাটা পড়ার কাজ করা হয়, এখন আমরা
চাই এই ক্লাসের একটি অবজেক্ট যদি তৈরি করা থাকে তাহলে আর নতুন করে কোন অবজেক্ট তৈরি না করে যেটা তৈরি হয়ে আছে সেটাই রিটার্ন
করে দিব। এই ধরনের কাজগুলোর জন্যে ফ্যাক্টরি কন্সট্রাক্টর ব্যাবহার করা হয়ে থাকে । ডার্টে ফ্যাক্টরি কনস্ট্রাক্টর ডিক্লেয়ার
করতে `factory` কীওয়ার্ড ব্যবহার করা হয়,

```Java
class DatabaseConnection {
final String _url;

// Private constructor to create a database connection
DatabaseConnection._(this._url);

// Static map to store and reuse database connections
static final Map<String, DatabaseConnection> _connections = {};

// Factory constructor to get a database connection
factory DatabaseConnection(String url) {
if (_connections.containsKey(url)) {
return _connections[url]!;
} else {
final newConnection = DatabaseConnection._(url);
_connections[url] = newConnection;
return newConnection;
}
}

// Simulate opening a database connection
void open() {
print('Opened database connection to $_url');
}

// Simulate closing a database connection
void close() {
print('Closed database connection to $_url');
}
}

void main() {
final dbConnection1 = DatabaseConnection('example.com/db');
final dbConnection2 = DatabaseConnection('example.com/db');

// Both references should point to the same database connection
print(identical(dbConnection1, dbConnection2)); // true

dbConnection1.open();
dbConnection1.close();
}
```

## this কিওয়ার্ড

কন্সট্রাক্টর অধ্যায় এর পুরোটা জুড়ে আমরা অনেকবার `this` কিওয়ার্ডটি ব্যাবহার করেছি। সংক্ষেপে `this` কিওয়ার্ড এর কাজ হল
ক্লাসের
অবজেক্টকে নির্দেশ করা।

## ক্লাসের মেথড:

ক্লাসে কি শুধুই ভেরিয়েবলই রাখা যায়? উত্তর হল না, আমরা চাইলে ক্লাসের মধ্যে আমাদের প্রয়োজনীয় বিভিন্ন ফাংশন ও ডিক্লেয়ার করে
রাখতে পারি। একটি ক্লাসে ডিক্লেয়ার করা ফাংশন গুলোকে আমরা চিনব ক্লাসের মেথড হিসেবে । ক্লাসের অবজেক্ট এর মাধ্যমে ডিক্লেয়ার
করা মেথডগুলোকে ব্যাবহার করা যায়।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car({
required this.manufacturerCompany,
required this.color,
required this.numberOfSeats,
});

void printAllValuesInConsole(){
print('Manufacturer: $manufacturerCompany');
print('Color: $color');
print('Number Of Seats: $numberOfSeats');
}
}

void main() {
Car car = Car(
manufacturerCompany: 'Toyota',
color: 'Green',
numberOfSeats: 4,
);
car.printAllValuesInConsole();
}
```

আউটপুট:

```Java
Manufacturer: Toyota
Color: Green
Number Of Seats: 4
```

এখানে `car` অবজেক্টটি দিয়ে `Car` ক্লাসের `printAllValuesInConsole` এই মেথডটিকে ব্যাবহার করে `car` অবজেক্টটির ভ্যালু
গুলোকে
কনসোলে প্রিন্ট করা হল।

আমরা এখন পর্যন্ত শুধুমাত্র কন্সট্রাক্টর এর মাধ্যমে অবজেক্ট কে ইনিশিয়ালাইয করেছি এবং ক্লাসের ভেরিয়েবল গুলোতে ভ্যালু আসাইন
করেছি । কিন্তু ডার্ট আমাদেরকে দুইটি স্পেশাল ক্লাস মেথড দেয়, তারা হল সেটার এবং গেটার মেথড । সেটার মেথড এর মাধ্যমে ক্লাসের
কোন ফিল্ড/ভেরিয়েবল এর ভ্যালু ইনিশিয়ালাইয অথবা আপডেট করে দেওয়া যায় এবং গেটার মেথড এর মাধ্যমে কোন ফিল্ড/ভেরিয়েবল এর ভ্যালু
পড়তে পারা যায়। সেটার এবং গেটার মেথড এর আরেকটি ব্যাবহার হল ক্লাসের প্রাইভেট কোন ফিল্ড/ভেরিয়েবল কে পাবলিক সেটার এবং গেটার
মেথড এর মাধ্যমে ব্যাবহার করা।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car({
required this.manufacturerCompany,
required this.color,
required this.numberOfSeats,
});

set setColor(String color) => this.color = color;

String get getColor => this.color;

void printAllValuesInConsole(){
print('Manufacturer: $manufacturerCompany');
print('Color: $color');
print('Number Of Seats: $numberOfSeats');
}
}
```

আউটপুট:

```Java
Manufacturer: Toyota
Color: Green
Number Of Seats: 4
Updated color value: Red
```

এখানে `set` কিওয়ার্ড ব্যাবহার করে `setColor` নামে একটি সেটার মেথড তৈরি করা হয়েছে যার কাজ হল `color` ভেরিয়েবল এর ভ্যালু
সেট/অথবা আপডেট করা এবং `get` কিওয়ার্ড ব্যাবহার করে `getColor` নামে একটি গেটার মেথড তৈরি করা হয়েছে যার মাধ্যমে `color`
ভেরিয়েবল
এর ভালু পড়তে পারা যাবে।

# ইনহেরিট্যান্স এবং পলিমরফিসম:

## ইনহেরিট্যান্স

ইংলিশ শব্দ `inheritance` এর একটা বাংলা অর্থ হচ্ছে উত্তরাধিকার সূত্রে কিছু পাওয়া। অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং এ ক্লাস
গুলোর মধ্যে কিছু ফাংশনালিটি ও বৈশিষ্ট্য শেয়ার করার একটা পদ্ধতি হচ্ছে ইনহেরিট্যান্স। অর্থাৎ, একটা ক্লাসকে ইনহেরিট (
অনুসরণ) করে তার কিছু বৈশিষ্ট্য আরেকটি উত্তরসূরি ক্লাসের মধ্যে নিয়ে আসার ব্যাপারটিকেই ইনহেরিট্যান্স বলা হয়।

ডার্ট এ কোন ক্লাসকে ইনহেরিট করার জন্যে `extend` কিওয়ার্ড ব্যাবহার করা হয়।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany,
this.color,
this.numberOfSeats,
);

set setColor(String color) => this.color;

String get getColor => this.color;

void printAllValuesInConsole() {
print('Color: $color');
print('Number Of Seats: $numberOfSeats');
}
}

class BmwCar extends Car {
String bmwModel;

BmwCar(
String manufacturerCompany,
String color,
int numberOfSeats,
this.bmwModel,
) : super(manufacturerCompany, color, numberOfSeats);

void printBMWCarProperties() {
print('Manufacturer Company: $manufacturerCompany');
print('Color: $color');
print('Number Of Seats: $numberOfSeats');
print('BMW Model: $bmwModel');
}
}

void main() {
BmwCar bmwCar = BmwCar(
'BMW',
'Black',
4,
'Electric Luxury Sedan',
);
bmwCar.printBMWCarProperties();
}
```

আউটপুট:

```Java
Manufacturer Company: BMW
Color: Black
Number Of Seats: 4
BMW Model: Electric Luxury Sedan
```

এখানে `Car` ক্লাসটিকে `extend` করে আমরা একটি নতুন ক্লাস তৈরি করলাম `BmwCar` , এই নতুন ক্লাসটিতে আমরা `bmwModel`
ভ্যারিয়েবল টি
যোগ করে আদতে `BmwCar` ক্লাসে নতুন একটি বৈশিষ্ট্য যোগ করলাম। `BmwCar` যেহেতু `Car` ক্লাসকে ইনহেরিট করেছে কাজেই এই ক্লাসটি
এখন
`Car` ক্লাসের সব বৈশিষ্ট্য এবং তার নিজের বৈশিষ্ট্য নিয়ে কাজ করবে।

ডার্ট মাল্টিপল ইনহেরিট্যান্স সাপোর্ট করে না , এর মানে হল একটা ক্লাস একের অধিক ক্লাসকে একসাথে ইনহেরিট করতে পারবেনা ।  
সুপার কিওয়ার্ড:  
ডার্টে, সুপার কীওয়ার্ড ব্যবহার করা হয় প্যারেন্ট ক্লাসকে নির্দেশ করতে, প্যারেন্ট ক্লাসের মেথড এবং প্রপার্টি গুলোকে কল
করতে হলে সুপার কীওয়ার্ড ব্যবহার করা হয় ।

## পলিমরফিজম:

পলিমরফিজম হলো বহুরূপতা । প্রোগ্রামিং এ পলিমরফিজম বলতে বোঝা য় একই ফাংশন কে ভিন্ন ভাবে ব্যবহার করা বা ভিন্ন আচরণ করা।
ডার্টে মেথড অভাররাইডিং এর মাধ্যমে আমরা পলিমরফিজম এর প্রয়োগ দেখব ।  
প্যারেন্ট ক্লাসে ডিক্লেয়ার করে আসা কোন মেথড কে চাইল্ড ক্লাস যদি তার মত করে ব্যাবহার করে তাহলে বলা যায় যে চাইল্ড ক্লাস
প্যারেন্ট ক্লাসের মেথড অভারাইড করেছে । আমরা উদাহরণ এ চলে যাই।

```Java
class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany,
this.color,
this.numberOfSeats,
);

void power() {
print('Car runs on oil.');
}
}

class BmwCar extends Car {
String bmwModel;

BmwCar(
String manufacturerCompany,
String color,
int numberOfSeats,
this.bmwModel,
) : super(manufacturerCompany, color, numberOfSeats);
}

class TeslaCar extends Car {
TeslaCar(
String manufacturerCompany,
String color,
int numberOfSeats,
) : super(manufacturerCompany, color, numberOfSeats);

@override
void power() {
print('Tesla car runs on electricity.');
}
}

void main() {
BmwCar bmwCar = BmwCar(
'BMW',
'Black',
4,
'Electric Luxury Sedan',
);
bmwCar.power();

TeslaCar teslaCar = TeslaCar(
'Tesla',
'Black',
4,
);

teslaCar.power();
}
```

আউটপুট:

```Java
Car runs on oil.
Tesla car runs on electricity.
```

সাধারণত `Car` চলে তেল এ। এই কারনে `Car` ক্লাসে একটি কমন বৈশিষ্ট্য যোগ করা হয়েছে `power()` এবং এই মেথডে আমরা দেখতেছি যে
`Car,runs on oil` । এখন টেসলা গাড়ি কিন্তু চলে ইলেক্ট্রিসিটিতে এবং তাকে তেলে চালানো যাবে না । এই সমস্যার সমাধানের জন্যে
আমাদের `Car` ক্লাসের `power()`  মেথডকে নতুন একটি রূপ দিতে হবে যাতে সে টেসলা গাড়িকে ইলেক্ট্রিসিটি দিয়ে চালাতে
পারে । `TeslaCar`
ক্লাস `Car` ক্লাসের `power()` মেথডকে অভাররাইড করে এই মেথডকে নতুন একটি রূপ দিল যেখানে আমরা দেখছি `Tesla car runs on
electricity`. এটিই হল পলিমরফিসম।

## অ্যাবস্ট্রাকশন এবং এনক্যাপসুলেশন:

অবজেক্ট-অরিয়েন্টেড প্রোগ্রামিংয়ের চারটি মৌলিক প্রিন্সিপল মধ্যে একটি হল অ্যাবস্ট্রাকশন। অ্যাবস্ট্রাকশন এর মাধ্যমে কোন
একটি সিস্টেমের জটিল কাজগুলোকে লুকিয়ে রেখে বেবহারকারিদের কাছে শুধু মাত্র প্রয়োজনীয় বিষয় গুলোই তুলে ধরা হয়।
অবজেক্ট-অরিয়েন্টেড প্রোগ্রামিংয়ে অ্যাবস্ট্রাক ক্লাস , ইন্টারফেস এবং এনক্যাপসুলেশন এর মাধ্যমে অ্যাবস্ট্রাকশন প্রয়োগ করা
যায় । ডার্টে অ্যাবস্ট্রাকশন প্রয়োগ করার জন্যে `abstract` ক্লাস ব্যাবহার করা হয়ে থাকে । আমরা 'abstract' কীওয়ার্ড ব্যবহার
করে `abstract` ক্লাসটি ঘোষণা করতে পারি। অ্যাবস্ট্রাক ক্লাসে এক বা একাধিক অ্যাবস্ট্রাক মেথড (যে মেথড গুলোর কোন
ইমপ্লিমেন্টেশন দেওয়া থাকে না ) থাকতে পারে ।  
অ্যাবস্ট্রাক ক্লাসে এক বা একাধিক অ্যাবস্ট্রাক মেথড (যে মেথড গুলোর কোন ইমপ্লিমেন্টেশন দেওয়া থাকে না ) থাকতে পারে ।
অ্যাবস্ট্রাক ক্লাসের কোন ইন্সটেন্স তৈরি করা যায় না, অ্যাবস্ট্রাক ক্লাসকে কোন একটি সাবক্লাস `extend` / `implement` করে
এবং
সাবক্লাসটির দায়িত্ব থাকে অ্যাবস্ট্রাক মেথডগুলোর ইমপ্লিমেন্টেশন দেওয়া
আমরা একটি কোড স্যাম্পল দেখে ফেলি:

```Java
abstract class Car {
String manufacturerCompany;
String color;
int numberOfSeats;

Car(
this.manufacturerCompany,
this.color,
this.numberOfSeats,
);

void power();
}

class BmwCar extends Car {
String bmwModel;

BmwCar(
String manufacturerCompany,
String color,
int numberOfSeats,
this.bmwModel,
) : super(manufacturerCompany, color, numberOfSeats);

@override
void power() {
print('BMW runs on oil');
}
}

class TeslaCar extends Car {
TeslaCar(
String manufacturerCompany,
String color,
int numberOfSeats,
) : super(manufacturerCompany, color, numberOfSeats);

@override
void power() {
print('Tesla runs on electricity.');
}
}

void main() {
BmwCar bmwCar = BmwCar(
'BMW',
'Black',
4,
'Electric Luxury Sedan',
);
bmwCar.power();

TeslaCar teslaCar = TeslaCar(
'Tesla',
'Black',
4,
);

teslaCar.power();
}
```

আউটপুট :

```Java
BMW runs on oil
Tesla runs on electricity.
```

এখানে `TeslaCar` এবং `BmwCar` অ্যাবস্ট্রাক `Car` ক্লাসকে এক্সটেন্ড করে অ্যাবস্ট্রাক মেথড `power()` কে নিজেদের মতন করে
ইমপ্লিমেন্ট করে নিয়েছে

**এনক্যাপসুলেশন** হল অবজেক্ট-অরিয়েন্টেড প্রোগ্রামিংয়ের আরেকটি গুরুত্বপূর্ণ বৈশিষ্ট্য , একটি ক্লাসের শুধুমাত্র
প্রয়োজনীয়
মেথড এবং প্রপার্টিজ গুলোকে ব্যাবহার করতে দিয়ে এনক্যাপসুলেশন একটি ক্লাসের নিরাপত্তা কে নিশিত করে থাকে । এনক্যাপসুলেশন এর
মাধ্যমে সহজেই কোন একটি ক্লাসের নিজস্ব বৈশিষ্ট্য কে বদলানো যায় , পুরো সিস্টেম এর উপরে কোন ইমপ্যাক্ট না ফেলেই
এক্সেস মডিফায়ার এর মাধ্যমে আমরা একটি ক্লাসে প্রাইভেট প্রপার্টি অথবা মেথড কে প্রাইভেট হিসেবে ডিক্লেয়ার করে এনক্যাপসুলেশন
প্রয়োগ করতে পারি । ডার্টে _ এর মাধ্যমে এটি ব্যাবহার করা যায় ।

```Java
class Car {
String _color; // Private field for car color

Car(this._color);

// Getter for car color
String get color => _color;

// Setter for car color
set color(String color) {
_color = color;
}
}

void main() {
var myCar = Car('Red');

// Accessing and modifying the private field using getter and setter
print('Car Color: ${myCar.color}'); // Access using getter
myCar.color = 'Blue'; // Modify using setter
print('Updated Car Color: ${myCar.color}');
}
```

আউটপুট :

```Java
Car Color: Red
Updated Car Color: Blue
```

## এনুমেরেশন:

এনুমেরেশন বা সংক্ষেপে এনাম হচ্ছে বিশেষ একটি ক্লাস যার মাধ্যমে কিছু নির্দিস্ট সংখ্যক কন্সটান্ট ভ্যালু কে নির্দেশ করা
যায় । একটি `enum` ডিক্লেয়ার করার জন্য `enum` কীওয়ার্ড ব্যবহার হয়। এনাম তৈরির সময় এর ভ্যালু গুলো বলে দিতে হয়। এই
স্পেশাল
টাইপ ভ্যারিয়েবল গুলো সাধারণত সুইচ এবং কনডিশনালের সাথে ব্যবহৃত হয়।
উদাহরণ স্বরূপ, এই কোডে একটি `enum` তৈরি করা হল :

```Java
enum Color {
red,
green,
blue,
yellow,
}

void main() {
Color myColor = Color.blue;

if (myColor == Color.red) {
print('Color is Red');
} else if (myColor == Color.blue) {
print('Color is Blue');
} else {
print('Color is not Red or Blue');
}
}
```

এই `enum Color` একটি নামক ডেটা টাইপ তৈরি করে, এবং এটির কন্সটান্ট কিছু ভ্যালু আছে  `(red, green, blue, yellow)।
`

 

