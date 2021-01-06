## BufferedReader 
- 데이터를 바로 전송하는 Scanner에 비해 버퍼를 이용하여 한번에 전송하므로 효율적임
- Scanner보다 알고리즘 면에서 효율적이지만 사용법이 복잡함
- 입력값이 String값으로 들어오므로 형변환 필수

### 사용 예시
```
try { // 예외처리 때문에 try catch문이나 throws를 사용해야 함
  BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // BufferedReader 생성
  String input = br.readLine(); // 값 입력 (String값)
  char array[] = input.toCharArray(); // (번외) String 문자열을 하나씩 char형 배열에 삽입

  br.close();
} catch (IOException e) {
  e.printStackTrace();
} 
```


## BufferedWriter
- BufferedReader와 마찬가지로 버퍼를 사용하며 System.out.print();에 비해 알고리즘 면에서 효율적임
- 출력 시 개행이 되지 않으므로 따로 시행해야 함

### 사용 예시
```
BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
String output = "hello";

bw.write(output);
bw.newLine(); // 개행
bw.write(output + "\n");  // 개행 2

bw.flush();
bw.close();
```
