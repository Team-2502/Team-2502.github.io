---
layout: post
title: Using JavaDoc
category: General
---
In the event that another person must use or read your code, they must be able to easily understand how it works.

Using JavaDoc is a nice way to make your code easily readable.

# JavaDoc

The JavaDoc is a useful tool that can explain a method when you mouse over it in Eclipse. To do so in IntelliJ, the setting is found under `Editor -> General -> Other -> Show quick documentation on mouse move`. Alternatively, look at your keymap and remember the key for showing documentation.

## Adding a JavaDoc to your class methods

Suppose we have the class



    public class Wiki
    {
        public Wiki()
        {
            //do stuff
        }
        public Wiki(double a)
        {
            //do stuff
        }
        public boolean isMicrowaveOn(String microwaveName)
        {
            //do stuff
        }
    }

and we want to add a JavaDoc to it. To do so, before each constructor and method, we type

    /**

and press enter. In Eclipse and IntelliJ, this automatically fills out the comment for the javadoc. If we did this for all the constructors and methods in Wiki.java, we would have


    public class Wiki
    {
        /**
         *
         */
        public Wiki()
        {
            //do stuff
        }
        /**
         *
         * @param a
         */
        public Wiki(double a)
        {
            //do stuff
        }
        /**
         *
         * @param microwaveName
         * @return
         */
        public boolean isMicrowaveOn(String microwaveName)
        {
            //do stuff
        }
    }

Now, in each JavaDoc comment, which should show up blue in Eclipse, we may type what we want to show to the user about what each thing does. This will show up when another programmer mouses over the method.

### JavaDoc Decorators

There are 2 decorators we will explain in this wiki page.

* `@param`

* `@return`

### `@param`

The decorator `@param` must have a parameter name after it. For example, the javadoc entry for `Wiki.isMicrowaveOn` has an `@param` followed by the name of the parameter, `microwaveName`. If we put a space after `@param microwaveName`, we may put an explanation about what that variable does. In this case, it specifies which microwave we should check is on. So, our full decorator looks like

    @param microwaveName Which microwave we should check is on

### `@return`

The decorator `@return` explains what the method returns, if it returns anything. In this case, it returns a boolean that says whether or not the microwave is on. So, the `@return` decorator for the method Wiki.isMicrowaveOn should say

    @return Returns a boolean that says whether or not the microwave is on


### Full javadoc annotation for Wiki.java

    public class Wiki
    {
        /**
         * Instantiates the wiki class with the default Microwave Voltage of 240V
         */
        public Wiki()
        {
            //do stuff
        }
        /**
         * Instantiates the wiki class with a customizable microwave voltage
         * @param a voltage of the microwave
         */
        public Wiki(double a)
        {
            //do stuff
        }
        /**
         * Tells you if the microwave is on
         * @param microwaveName Which microwave we should check is on
         * @return Returns a boolean that says whether or not the microwave is on
         */
        public boolean isMicrowaveOn(String microwaveName)
        {
            //do stuff
        }
    }
