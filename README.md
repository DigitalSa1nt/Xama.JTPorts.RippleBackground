# Xamarin Ripple Background
[![platform](https://img.shields.io/badge/platform-Xamarin.Android-brightgreen.svg)](https://www.xamarin.com/)
[![API](https://img.shields.io/badge/API-21%2B-orange.svg?style=flat)](https://android-arsenal.com/api?level=10s)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

# Namespace: Xama.JTPorts.RippleBackground

Animated ripple background for Xamarin.Android Ported from a Java library. You can adjust the ripple colours, the speed of the ripples as well as the amount of ripples.

## Fill Ripple

![!gif](https://github.com/DigitalSa1nt/Xama.JTPorts.RippleBackground/blob/master/images/20190217_220639.gif?raw=true)

## Stroke Ripple

![!gif](https://github.com/DigitalSa1nt/Xama.JTPorts.RippleBackground/blob/master/images/20190217_220842.gif?raw=true)

# How to Install

At the moment, until I create the nuget package you would need to download the src code, compile and build it, then simply reference the DLL in your Xamarin.Android Project. Or alternatively you could add the project as a project within your solution if you plan on adjusting any of the code for your own uses.

# Basic Usage

Simply define the ripple control in your AXML layout and wrap it around whatever you want. You can set the control to ripple on click, or you can disable that via the attribute 'rb_rippleOnClick' and set up your own way of starting the ripple effect by simply calling the following method `StartRippleAnimation();` on the ripple control object.

```cs
<Xama.JTPorts.RippleBackground.RippleBackground
     android:layout_width="match_parent"
     android:layout_height="match_parent"
     android:id="@+id/content"
     app:rb_radius="32dp"
     app:rb_rippleAmount="4"
     app:rb_duration="3000"
     app:rb_rippleColour="@color/colorAccent"
     app:rb_type="strokeRipple"
     app:rb_strokeWidth="1dp"
     app:rb_rippleOnClick="true"
     app:rb_scale="6">

     <ImageView
         android:layout_width="64dp"
         android:layout_height="64dp"
         android:layout_centerInParent="true"
         android:id="@+id/centerImage"
         android:src="@drawable/iconheartwatch"/>

</Xama.JTPorts.RippleBackground.RippleBackground>
```

The Paint.Color attribute used in the process of drawing the ripple circles has been changed to be a static property of the `RippleBackground` control. So you can set `.RippleColour` on the ripple control programatically and it will apply to all initialised ripples.

# Available Attributes

You can supply the following attributes:

| Attribute        | Type            | Purpose                 |
|------------------|-----------------|-------------------------|
| rb_rippleOnClick | bool            | Automatically sets up a ripple on click event with toggle |
| rb_rippleColour  | color/reference | This defines the fill or stroke colour of the ripple effect itself |
| rb_strokeWidth   | dimension       | If you choose a stroke ripple, this defines the ripple stroke widths |
| rb_radius        | dimension       | Radius of the ripples   |
| rb_duration      | integer         | Duration of the individual ripple animations in milliseconds |
| rb_rippleAmount  | integer         | Maximum amount of ripples |
| rb_scale         | float           | Scale of ripple at the end of one animation cycle |
| rb_type          | enum            | fillRipple/strokeRipple |


# Useful?
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=PFBEH42KW5P84" method="post" target="_top"><img src="https://camo.githubusercontent.com/b8efed595794b7c415163a48f4e4a07771b20abe/68747470733a2f2f7777772e6275796d6561636f666665652e636f6d2f6173736574732f696d672f637573746f6d5f696d616765732f707572706c655f696d672e706e67" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>

 _You know, only if you want to_
