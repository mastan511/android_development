# Activity and Fragment Overview

If you are new to Android development, you might have read up about activity and fragment and think they are similar. You may not be sure when to use one over the other.This doc is to help go over the basics of an activity and a fragment and see how they are similar and different.


## What Is an Activity
 

**An activity is a crucial component of an Android app. The way activities are launched and put together is a fundamental part of the Android platform application model. The Android system initiates code in an activity instance by invoking specific callback methods that correspond to specific stages of its lifecycle. This way of initialization is unlike other programming paradigms that launch with a main() method.**

 

## What Is a Fragment

**A fragment represents a behavior or a portion of the user interface in an Activity. You can have multiple fragments in an activity or you can reuse a fragment in multiple activities. You can think of a fragment like a modular section of an activity. It has its own lifecycle, receives its own input events, and you can add or remove them while the activity is running.**

 

**There are two ways for you to add a fragment into an activity. One is by adding the fragment into the activity’s layout file. Another is by adding it into an existing ViewGroup in your application code. When you add a fragment as part of the activity layout, it lives in a ViewGroup inside the activity’s view hierarchy and the fragment defines its own view layout.**

 

## Relationship Between an Activity and a Fragment
 

**A fragment must always be hosted in an activity and a fragment’s lifecycle is directly affected by the host activity’s lifecycle. For example, when an activity resumes so will all of its fragments and when the activity pauses so will all of the fragments. However, while an activity is running (resumed lifecycle state), you can freely manipulate the state of a fragment, such as add or remove them. Another way to look at it is that when a fragment changes state it doesn’t affect the activity, but when the activity changes state it does affect the fragment.**


**Activity and fragments operate under the one-to-many relationship. That is, you can have one activity and host many fragments on top of it. The opposite case does not hold true. In fact, a fragment can’t exist without an activity to be the host.**

 

## Similarities Between Activity and Fragment
 

**Both an activity and a fragment have their own lifecycle. They both also can be in one of the three states, which are resumed, paused, and stopped.**

 

# Differences Between Activity and Fragment
 

**The most significant difference between an activity and a fragment is how one is stored in its respective back stack. For an activity, the back stack is managed by the system and in most cases, you would not have to worry about it. An activity is placed into the back stack of activities when it’s stopped by default so that the user can navigate back to it with the back button.**

 

**A fragment, on the other hand, doesn’t get automatically added into the back stack. For a fragment to be added into the back stack, the host activity must explicitly request for the instance to be saved by calling addToBackStack during a transaction that removes the fragment.**

 
