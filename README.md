Objective-C Interop Sample
==========================

This sample shows how to expose managed classes in C# to Objective C libraries.

In this sample a very simple class (StringUtilities) is exposed to Objective C. It contains two
methods, to convert a string to upper or to lower case.

The steps to implement this are:

1) Read the limitations at the bottom of this page. This will likely affect the API you can/will
   expose.

2) Make sure the managed class to expose has the required attributes so that it's visible from
   Objective C. This is identical to how Objective C classes are exposed to managed code, as
   explained here: http://docs.xamarin.com/ios/advanced_topics/binding_objective-c_types/binding_details.
   See StringUtilities.cs for an example.

3) Create an Objective C header file, describing the managed class. This is just the inverse of
   step 2).

Now you can import the Objective C header file in your Objective source files, and just use the managed
class as if it were an Objective C class.

In this sample there is also an Objective C class that is exposed to C# (with a binding project),
and that Objective C class is used to test that everything works.

Limitations
----------
* Only instance methods can be exposed to Objective C.
* It is not possible to create managed classes in Objective C. You must create the managed class in C#, and then pass it to Objective C.

