# ERRER
[[ CS0176 ]]
<br>[ const ]는 [ instance reference ]로 accesse(엑세스) 불가, 대신 [ type(class) name ]으로 qualify(자격있다)를 한다.
<br>public class MyValues {
<br>---public const float testValue = 9.99f;
<br>}
<br>public class MyMain {
<br>---private MyValues _mV;
<br>---public void MyFunction() {
<br>------float errerValue = _mV.testValue //CS0176 ERRER
<br>------float possibleValue = MyValues.testValue //not errer
<br>---}
<br>}
<br><hr>
