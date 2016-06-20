# ASP.NET MVC Interview Questions

本篇資料來自 [Most Asked ASP.NET MVC Interview Questions and Answers](http://www.c-sharpcorner.com/uploadfile/8ef97c/most-asked-asp-net-mvc-interview-questions-and-answers/)

***Note***：利用 Repository 來練習，並整理自己會的觀念，敬請參考，有任何錯誤也請向我提出，感謝。

## What is MVC?
是一種 Framework，微軟在 ASP.NET 中所添加的一組類別庫，可以利用 View-Model-Controller 模式進行開發，利用路由 (Routing) 導向，來分析 URL，將程式導向正確的 Controller 與 Action，與原本的 ASP.NET 並不衝突，可以並行。
* View：呈現資料，與使用者互動。
* Model：傳接資料 (Model)、與 DB 資料結構呼應 (Entity)、驗證資料 (ViewModel)。
* Controller：負責中控的腳色，接收使用者資料，與呼叫所需要的 View 與方法 (Method)，或 return 使用者所需的資料。

## Why MVC is Better?



## Explain MVC application life cycle
1. 創建RouteTable (程式第一次啟動才會發生)：讓 URL 對應 Controller
2. UrlRoutingModule攔截請求：從 Route Table 中找到對應的 Controller
3. 執行MvcHandler：從 IControllerFactory 取得 Controller 實體
4. 執行控制器：執行 Controller Action
5. 調用RenderView方法：產生畫面，同時也包含 Razor Engine

## List out different return types of a controller action method

## What are Filters in MVC?

## What are Action Filters in MVC?

## Explain what is routing in MVC? What are the three segments for routing important?

## What is Route in MVC? What is Default Route in MVC?

## Mention what is the difference between Temp data, View data, and View Bag?
* Temp data 是 dictionary 型別，可以跨 Controller 仍然有效，與 Session 類似。
* View data 是 dictionary 型別，只在當前 Action 中有效，生命週期和 View 相同。
* View Bag 是 dynamic 型別，只在當前 Action 中有效，生命週期和 View 相同。

## What is Partial View in MVC?
如果說 View 是一個完整頁面，Partial View 就是 View 切出來做的其中一個部分。

## Explain what is the difference between View and Partial View?
View 會是一個完整的 HTML，而 Partial View 並不是，因為他要掛在某個 View 底下，所以不會有完整的 HTML。

## What are HTML helpers in MVC?
說簡單一點就是在 View 中，利用後端的語法幫助你產生前端的使用者控制項，像是 ActionLink, Textbox, Password...等等，也能夠自己擴充。 

## Explain attribute based routing in MVC?

## What is TempData in MVC?
Temp data 是 dictionary 型別，可以跨 Controller 仍然有效，與 Session 類似。

## What is Razor in MVC?
Rezor 是 MVC 3 開始的方法，有自己的 Razor 語法，幫助我們減少 code 的行數，一樣是可以 render server side 的資料，語法上為 `@your code`，可以預防 XSS (cross site script)攻擊。

## Differences between Razor and ASPX View Engine in MVC?
*  ASPX View Engine 是 WebForm 方法，語法與 C# 語法無異，來 render server side 的資料，語法上為 `<% //your code here %>`，無法預防 XSS (cross site script)攻擊
*  Rezor 是 MVC 3 開始的方法，有自己的 Razor 語法，幫助我們減少 code 的行數，一樣是可以 render server side 的資料，語法上為 `@your code`，可以預防 XSS (cross site script)攻擊。

## What are the Main Razor Syntax Rules?
在 View 中使用 @符號 + 語法，ex：@Model.content

## How do you implement Forms authentication in MVC?

## Explain Areas in MVC?
可以讓整個專案，依照功能模組切割多個 Area，讓 Controller 與 View 可以有更好的管理，不會全部都擠在一起。
建立一個 Area 就會有自己 Area 的 AreaRegistration.cs，提供此 Area 預設的 Route 設定，例如：BackendArea，則此 Area 的 AreaRegistration.cs 就會為：Backend/{controller}/{action}/{id}。

## Explain the need of display mode in MVC?
可以依照 clint 端的狀況，而選擇 return 給使用者 view 的機制。
* 依照使用者的 Browser
* 依照使用者的語系
* 使用者的螢幕大小 (手機版的 View)

## Explain the concept of MVC Scaffolding?

## What is Route Constraints in MVC?

## What is Razor View Engine in MVC?
在 View 上 render server side 的資料使用的方法，語法為`@YourCode`
此方式可以預防 XSS (cross site script) 攻擊
Razor 有自己的語法，會與 C# 語法上稍有不同

## What is Output Caching in MVC?

## What is Bundling and Minification in MVC?

## What is Validation Summary in MVC?

## What is Database First Approach in MVC using Entity Framework?

## What are the Folders in MVC application solutions?

## What are the methods of handling an Error in MVC?

## How can we pass the data From Controller To View In MVC?
1. 直接在 return View 的時候 使用 Razor 語法把資料 render 到畫面上
2. 利用前端 ajax 方式跟 controller 的 action 取得 json 資料，再由 javascript 處理畫面呈現給使用者

## What is Scaffolding in MVC?

## What is ViewStart?

## What is JsonResultType in MVC?

## What is TempData?
Temp data 是 dictionary 型別，可以跨 Controller 仍然有效，與 Session 類似。

## How to use ViewBag?
因為生命週期只有這個 View，所以通常會搭配 Razor 使用，型態為 dynamic，類似`@foreach(var item in ViewBag.Customer_OrderDetails)`

## What are the Difference between ViewBag&ViewData?
型態不同，ViewBag 是 dynamic 而 ViewData 是 dictionary，但生命週期是一樣的，都只有一個 View 的生命週期。

## What is Data Annotation Validator Attributes in MVC?

## How can we done Custom Error Page in MVC?

## Server Side Validation in MVC?

## What is the use of remote validation in MVC?

## What are the Exception filters in MVC?

## What is MVC HTML- Helpers and its Methods?

## Define Controller in MVC?
接收使用者資料，呼叫所有需要的方法、回給使用者需要的資料或畫面。

## Explain Model in MVC?
傳接資料、驗證資料、與 DB 結構呼應、商業邏輯。

## Explain View in MVC?
呈現使用者資料，與使用者互動。

## What is Attribute Routing in MVC?

## Explain RenderSection in MVC?

## What is GET and POST Actions Types?

## What's new in MVC 6?