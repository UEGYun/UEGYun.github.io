# Operators
[ 불리안 로지칼 오퍼레이토어스 ]
<br>( ! ) 유나리 로지칼 네개션 오퍼레이토어 => 단독 반대 평가.
<br>( & ) 바이나리 로지칼 앤드 오퍼레이토어 => 양쪽 모두 평가.
<br>( ^ ) 바이나리 익스클루시 오어 오퍼레이토어 => 양쪽 중에 반대 평가.
<br>( | ) 바이나리 로지칼 오어 오퍼레이토어 => 양쪽 중에 긍정 평가.
<br>( && ) 바이나리 콘디쇼날 로지칼 앤드 오퍼레이토어 => 앞 평가 긍정시만 다음 평가.
<br>( || ) 바이나리 콘디쇼날 로지칼 오어 오퍼레이토어 => 앞 평가 부정시만 다음 평가.
<br>
<br>연산우선순위 <=> ( ! ), ( & ), ( ^ ), ( | ), ( && ), ( || )
<br><hr>
[ 널레이블 불리안 로지칼 오퍼레이토어스 ]
<br>(( bool? )) 쓰리-발류드 로직 (true, null, false) => 세가지 평가.
<br>( & ) (모두 true == true, true말고 false없음 == null, true말고 false있음 == false)
<br><=> 트루 평가 1/9, 널 평가 3/9, 펄스 평가 5/9
<br>( | ) (양쪽 중에 true있음 == true, true없을때 null있음 == null, true없을때 모두 false == false)
<br><=> 트루 평가 5/9
<br>(( 사용 예 ))
<br>( ! ) bool a = !true;  bool b = !(value==0);   bool c = a && b;
<br>( & ) bool a = true & (value==0);
<br>( | ) bool a = true | (value==0);
<br>( ^ ) bool a = true ^ (value==0);
<br>( && ) bool a = true && (value==0);
<br>( || ) bool a = true || (value==0);
<br>( bool? ) bool? a = true & (value==0) | null;
<br><hr>
