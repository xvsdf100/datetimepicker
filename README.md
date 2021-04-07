##补充
ie8 不能赋值问题【ie8 jquery要2.0以下的版本】
```
            $('#test').on('blur', function(e){
                console.log("test blur")
                e.stopImmediatePropagation()
            })
```
在ie8选择时间就触发blur事件，这个事件会导致时间选择器先关闭，从而导致无法赋值，我分析半天代码，算是一个解决方案吧。暂时这样子，没有发现其他的问题。
test 是 测试iput的 id.

# jQuery DateTimePicker
[Demo and Documentation](https://xdsoft.net/jqplugins/datetimepicker/)

[![Build Status](https://travis-ci.org/xdan/datetimepicker.svg?branch=master)](https://travis-ci.org/xdan/datetimepicker)
[![npm version](https://badge.fury.io/js/jquery-datetimepicker.svg)](https://badge.fury.io/js/jquery-datetimepicker)
[![npm](https://img.shields.io/npm/dm/jquery-datetimepicker.svg)](https://www.npmjs.com/package/jquery-datetimepicker)



PLEASE. Help me update documentation.
[Doc.tpl](https://github.com/xdan/datetimepicker/blob/master/doc.tpl)
This file will be automatically displayed on the site

# Installation

```bash
npm install jquery-datetimepicker
```
OR
```bash
yarn add jquery-datetimepicker
```
or download [zip](https://github.com/xdan/datetimepicker/releases)
# datetimepicker
==============

**!!! The latest version of the options 'lang' obsolete. The language setting is now global. !!!**

Use this:
```javascript
jQuery.datetimepicker.setLocale('en');
```
[Documentation][doc]

jQuery Plugin Date and Time Picker

DateTimePicker

![ScreenShot](https://raw.github.com/xdan/datetimepicker/master/screen/1.png)

DatePicker

![ScreenShot](https://raw.github.com/xdan/datetimepicker/master/screen/2.png)

TimePicker

![ScreenShot](https://raw.github.com/xdan/datetimepicker/master/screen/3.png)

Options to highlight individual dates or periods

![ScreenShot](https://raw.github.com/Mingpao/datetimepicker/master/screen/4.png)

![ScreenShot](https://raw.github.com/Mingpao/datetimepicker/master/screen/5.png)

![ScreenShot](https://raw.github.com/Mingpao/datetimepicker/master/screen/6.png)

[doc]: https://xdsoft.net/jqplugins/datetimepicker/

### JS Build help

**Requires Node and NPM** [Download and install node.js](http://nodejs.org/download/).

Install:

1. Install `bower` globally with `npm install -g bower`.
2. Run `npm install`. npm will look at `package.json` and automatically install the necessary dependencies. 
3. Run `bower install`, which installs front-end packages defined in `bower.json`.

Notice: If you use Bower v1.5.2, you will get error: `The "main" field cannot contain minified files`
You can regress to version 1.3.12

1. `npm uninstall bower -g`
2. `npm install -g bower@1.3.12`

Build:

First install npm requirements: `npm install -g uglifycss concat-cli`
Then build the files: `npm run build`

When build completed, you'll have the following files:
- **build/jquery.datetimepicker.full.js** - browser file
- **build/jquery.datetimepicker.full.min.js** - browser minified file
- **build/jquery.datetimepicker.min.js** - amd module style minified file
