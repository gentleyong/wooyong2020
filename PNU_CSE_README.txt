기존 프레임워크에서 수정된 부분

1. darknetz/ta/connected_layer_TA.c​ --------> layer_TA make_connected_layer_TA_new() 함수
​
102 line l.inputs = inputs 바로 뒤에 
​
l.inputs = (l.inputs+1)/2;
​
추가
​
2. darknetz/host/examples/classifier.c​ ------> train_classifier() 함수
​
211 line의 조건문에
​
기존 조건문에 괄호 씌워주고 && (*net->seen < 10000)
​
추가
​
3. darknetz/ta/include/user_ta_header_defines.h
​
매크로변수
​
TA_DATA_SIZE 10 * 1024 * 1024 --> 2 * 1024 * 1024

변경