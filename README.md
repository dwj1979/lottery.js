## Lottery.js

🎲 A simple javascript lottery app.

<a target='_blank' rel='nofollow' href='https://app.codesponsor.io/link/6s5iGzH6BxpKb3dUFe3XDoT2/meetmore/lottery.js'>
  <img alt='Sponsor' width='888' height='68' src='https://app.codesponsor.io/embed/6s5iGzH6BxpKb3dUFe3XDoT2/meetmore/lottery.js.svg' />
</a>

[Chinese README](https://github.com/meetmore/lottery.js/blob/master/README.CN.md)  

## Screenshots
![lottery-demo](https://user-images.githubusercontent.com/978810/31418459-b21d6984-adfb-11e7-8fd8-7e9fc089ccfc.gif)

## [LiveDemo ->](https://meetmore.github.io/lottery.js/)
   
## Features
 - Flexible
 - Out of the box
 - Interesting Animation Effects
   
## Usage

 Prepare data like this
 
```js
    [
        {
            "avatar": "//example.com/avatar_1.jpg", 
            "name": "MeetMore",
            "data": {
                "title": "Front-End Developer",
                "company": "Little Apple",
                ……
            }
        },
        ……
    ]
```

 import CSS/JS

```html
    <!-- Zepto or jQuery -->
    <script src="http://zeptojs.com/zepto.min.js"></script>

    <link rel="stylesheet" href="./lottery.min.css" />
    <script src="./lottery.compact.min.js"></script>
```

 Call function and Ready to go


```js
    $.lottery({ 
        api:"./api.json" 
    });
```

## Config


```js
    $.lottery({ 
        el: ".lottery",                           // where we put dom，jquery selector
        timeout: 10,                              // time to auto stop（second）
        once: true,                               // winner can not repeatable
        title: "company",                         // the title will show in winner screen data[key]
        subtitle: "title",                        // the subtitle will show in winner screen data[key]
        api: 'http://example.com/lottery.json',   // API URL
        data: {},                                 // directly use userdata object (when use this, keep api empty)
        confetti: true,                           // show confetti effects
        showbtn: true,                            // show control button
        fitsize: true,                            // show all user in one screen
        speed: 400,                               // interval time to next candidate, the unit is ms
        number: 3                                 // how many winner will be get at one time
    });
```

 Parameter | Explain | Default | Optional
----|------|----|----
el | where we put dom  | body | jquery selector，e.g.”.lottery“
timeout | time to auto stop（second）  | null | 10 (int，second)
once | winner can not repeatable  | false | true (enable)
title | the title will show in winner screen  | user['name'] | user['data'][**key**] (key content in data fields)
subtitle | the subtitle will show in winner screen  | user['company'] | user['data'][**key**] (key content in data fields)
api | API JSON URL  | null | URL
data | directly use userdata object (when use this, keep api empty)  | null | Object
confetti | show confetti effects (if disable, confetti.js is not required)  | true | false
showbtn | show control button  | true | false
fitsize | fit user avatar size to show all user in one screen  | true | false
speed | interval time to next candidate, the unit is ms  | 350 | false
number | how many winner will be get at one time  | 1 | int

## API


```js
    $.lottery('start'); 
    $.lottery('stop');
    $.lottery('getUsers'); 
    $.lottery('winners', 'get');
    $.lottery('winners', 'clean');
    $.lottery('history', 'show');
    $.lottery('history', 'get');
    $.lottery('history', 'clean');
```

 Parameter | Explain | Return
----|------|----
start | startLottery | true
stop | stopLottery | Object，WinnerUser's info
getUsers | get user list | Object，Userlist
winners, get | get winners list | Object，Winnerslist
winners, clean | clean ignore user who has won | true
history, show | show the history screen | true
history, get | get history lottery list | Object，Historylist
history, clean | clean history lottery list | true
  
**Winners will be lose after refeash page, History will be save at LocalStorage.**
  
## Browser Support

- Modern Browser
   
## License

Copyright © Duohui.co - Apache License 2.0

## Credits

- confetti.js is created by [Javier Sosa](http://jsfiddle.net/Javalsu/vxP5q/743/)
- Icons are created by [Okay: Yasir B. Eryılmaz](https://thenounproject.com/term/okay/114615/), [Crown: Pundimon](https://thenounproject.com/term/crown/1028402), [Dice: davidyu](https://thenounproject.com/term/dice-point-4/1250653/) from the Noun Project
- Move.js is created by [TJ Holowaychuk](https://visionmedia.github.io/move.js/)
