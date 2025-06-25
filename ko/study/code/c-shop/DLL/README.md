# Dynamic Link Library
[ ERRER's ]
<br>=> 작동 안함
<br>public struct Sample {
<br>---public int value = default;
<br>---public int Set(int set) { Value = set; return Value; }
<br>---//return 값은 set 값으로 출력 되지만 Value가 변경되지 않고 항상 default 상태.
<br>}
<br>=> Unloading broken assembly Assets/---/---/MyDLL.dll, this assembly can cause crashes in the runtime
<br>public struct Sample {
<br>---public int Value { get; private set; }
<br>}
<br>
<br>
<br>
<br>
<br>
<br>
<br><hr>
