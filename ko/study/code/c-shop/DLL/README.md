# Dynamic Link Library
[ ERRER's ]
<br>=> 작동 안함
<br>public struct Sample {
<br>---public int value = default;
<br>---Set(int set) { Value = set; return Value; } //Value가 변경되지 않고 항상 default 상태.
<br>---private int Plus() { Value++;  return Value; } //이건 왠지 모르지만 작동 함.
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
