# Dynamic Link Library (DLL)
[[ ERRER's ]]
<br>public struct Sample {
<br>---public int value = default;
<br>---public int Set(int set) { Value = set; return Value; }
<br>}
<br>=> 프로그램에서 [ public static Sample UseSample = new(); ] 이렇게 사용하면
<br>return 값은 set 값으로 출력 되지만 Value가 변경되지 않고 항상 default 상태.
<br>해결책[ struct를 class로 바꾸거나 프로그램에서 static을 제거 하면 된다. 이유는 모름. ]
<br>
<br>public struct Sample {
<br>---public int Value { get; private set; }
<br>}
<br>=>이렇게 사용하면 에러가 발생한다. 이유는 모름.
<br>[ ERRER: Unloading broken assembly Assets/---/---/MyDLL.dll, this assembly can cause crashes in the runtime. ]
<br>
<br>public struct Sample {
<br>---public static string MyString {
<br>------get => MyString;
<br>------set { MyString = value ?? ""; } 
<br>---}
<br>}
<br>=>이렇게 사용하면 value를 못찾고 MyString에 무한 대입 하는 듯.
<br>[ ERRER: StackOverflowException: The requested operation caused a stack overflow. ]
<br><hr>
<br>[[ Bug's ]]
<br><hr>
