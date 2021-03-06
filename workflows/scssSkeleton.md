## scss 結構調整

* home.scss
* _variables.scss
* _basic.scss
* _layout.scss
* adMiner
  * _index.scss 
  * adMgmt
    * _admgmt.scss
  * trackMgmt
    * _trackMgmt.scss
  * audience
    * _audience.scss
  * report
    * _report.scss
  * dashboard
    * _dashboard.scss
  * eventLog
    * _eventLog.scss
  * adCreateAndEdit (adCampaign, adCreative, adGroup, adSet)
    * _adCampaign.scss
    * _adCreative.scss
    * _adGroup.scss
    * _adSet.scss
  * user
    * _user.scss
  * common
    * _*.scss
  * directive
    * _*.scss 


### home.scss

負責 import 所有檔案

### variables.scss

只存放共用變數 (e.g. color-white: #ffffff;)

### basic.scss

我們系統的基本樣式, 以及可以使用的 @mixin, @extend 等等

命名方式以 'dash' 為準

e.g. 

```
// class
.btn {
  outline: none;
}

// extend
%btn{
  outline: none;
}

// mixin
@mixin center-block() {
  outline: none;
}

```

### layout.scss

放置 header.scss 以及 footer.scss

### adminer資料夾

   style/adminer 資料夾結構大致如同 template
   
:: index.scss

home page 的頁面 scss

:: common

共用的 lib 的 scss

:: directive

共用的 directive 的 scss

e.g. _pmdComponents.scss

directive 當作個別的 lib, 變數請命名在自己的檔案裡面, 並使用全域變數。

e.g. $aaa-default-color: $color-red;

:: adCreateAndEdit

每個階段的 scss ( adCampaign, adSet, adCreative, adGroup )

:: adminer內的其他的資料夾

目前規劃只會有一個 scss， 並希望以一個 id 劃分區塊

e.g.

```
#audience {

}
#audience-create{

}
#audience-edit{

}
```

希望大家多用 `compass`

http://compass-style.org/

## Note:
1. 層數請在 4 層內
2. 如有 4 層解決不了的問題，請給註解
