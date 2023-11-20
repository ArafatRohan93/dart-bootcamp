# Unit Testing in Dart

By Shadman Sakib

# ডার্ট প্রোগ্রামিং - ইউনিট টেস্টিং

ইউনিট টেস্টিং এর সাহায্যে একটি অ্যাপ্লিকেশনের প্রতিটি পৃথক ইউনিট টেস্ট করা হয়।কমপ্লেক্স অ্যাপ্লিকেশনের ছোট ছোট অংশ আমরা
এর সাহায্যে টেস্ট করতে পারি পুরো অ্যাপ্লিকেশানটাকে রান না করেই।

ইউনিট টেস্টিং এর জন্যে ডার্টে test নামের একটি এক্সটারনাল লাইব্রেরি আছে। আমরা এই লাইব্রেরি দিয়ে কিভাবে ইউনিট টেস্টিং
লিখতে হয় সেটা ধাপে ধাপে দেখব।

* **ধাপ ১ঃ `test` প্যাকেজ প্রোজেক্টে যেভাবে অ্যাড করতে হয়**

প্রথমে আমরা pubspec.yaml ফাইলে নিচের মত করে `test` প্যাকেজ অ্যাড করব।

```Java
dependencies:
test:
```

তারপর আমরা `get dependencies` এ প্রেস করে প্যাকেজটি ইন্সটল করে নিব।

* **ধাপ ২ঃ `import` করব যেভাবে **

আমরা আমাদের কোডের যে ফাইল গুলিতে টেস্ট কোডে লিখব সেখানে নিচের মত করে import করব

```Java
import "package:test/test.dart";
```

* **ধাপ ৩ঃ যেভাবে tests লিখব**

আমরা শুরতে নিচের syntax টা দেখি।

```Java
test("Description of the test ", () {  
expect(actualValue , matchingValue)
});
```

এখানে আমরা `test` নামে একটা top-level ফাংশন দেখতে পাচ্ছি। description এ আমরা কি টেস্ট করব সেটা লিখে দিব যাতে অন্য কেও
কোড
রিড করে বুঝতে পারে। `expect` ফাংশন দিয়ে আমরা assertion এর কাজ করব।

কিছু ক্ষেত্রে আমরা এমন চাইতে পারি যে রিলেটেড টেস্টগুলি একটি গ্রুপের মধ্যে থাকবে। এজন্যে আমরা নিচের মত করে `group` syntax
ইউজ করব।

```Java
group("some_Group_Name", () {
test("test_name_1", () {
expect(actual, equals(expected));

});  
test("test_name_2", () {
expect(actual, equals(expected));
});
})
```

> যখন আমরা ইউনিট টেস্ট লিখি সেটাকে তিন অংশে ভাগ করে নিতে পারি। এটাকে অনেকটা টেস্টিং কোড কনভেনশন বলা যেতে পারে। এগুলা
> হচ্ছে
**arrange**, **act** এবং **assert** ।
> নিচের উদাহরন গুলিতে আমরা কোডে কমেন্ট করে দিব।

## উদাহরন ১ঃ একটি passing টেস্ট

আমরা বিয়োগ কার জন্যে একটি `subtract` মেথড এবং এটার টেস্ট কোড লিখব।

```Java
import 'package:test/test.dart';      
// Import the test package

int Subtract(int x,int y)                  
// Function to be tested {
return x-y;
}  
void main() {
// Define the test
test("test to check subtract method",(){  
// Arrange
var expected = 10;

      // Act 
      var actual = Add(30,20); 
      
      // Assert 
      expect(actual,expected); 

});
}
```

এটার output আসবে নিচের মত।

```Java
00:00 +0: test to check add method
00:00 +1: All tests passed!
```

## উদাহরন ২ঃ একটি Failing টেস্ট

এখন আমরা `subtract` মেথডটা এভাবে লিখব যাতে লজিকাল ভুল থাকবে এবং এটা আমরা টেস্ট করব।

```Java
import 'package:test/test.dart';

int Sub(int x,int y){
return x-y-1;
}  
void main(){
test('test to check sub',(){
var expected = 10;   
// Arrange

      var actual = Sub(30,20);  
      // Act 
      
      expect(actual,expected);  
      // Assert 

});
}
```

এটার আউটপুট নিচের মত আসবে।

```Swift
package:test expect
test.dart 14:3 main.<fn>

Expected: <10>
Actual: <9>
```

এভাবে আমরা ইউনিট টেস্টিং করে লজিকাল ভুল আছে কিনা যাচাই করতে পারি। 
