프로그램 실행 방법: Advanced IPC 기법(message passing)을 이용한 버전
1. 소스코드를 압축 해제한 디렉토리로 이동한 뒤 make 명령어를 수행하여 프로그램을 빌드한다.
2. 최종 생성된 프로그램의 이름은 paint이다. 그리는 측은 -w, 문제를 맞추는 측은 -r 옵션을 주어 실행한다.
3. Advanced IPC 기법(message passing)을 이용한 버전에서는 ./paint -w를 먼저 실행하고 그 다음 ./paint -r를 실행해야 한다.
4. 그림을 그리는 측(writer)에서 제시어를 입력하면, 정답을 맞히는 측(reader) 프로세스에서 문제가 제출되었음을 알리는 문구를 확인할 수 있다.
5. writer가 그림을 그리면 reader는 그 과정을 실시간으로 확인한다. reader는 콘솔에 단어를 입력하고 확인 받을 수 있다. 단어가 정답과 일치하면 writer와 reader의 두 프로세스 모두 즉시 종료한다.


추가(주의사항): 빌드하는 과정에서 stray 에러가 발생할 수 있습니다. 이는 소스코드 중간에 인코딩 방식이 다른 문자열(한글 주석)이 섞여 있기 때문입니다. (gcc 옵션을 다르게 주는 방법이 있는지는 모르겠으나) 한글 주석을 전부 지우고 컴파일해야 합니다. 소스코드에서 주석을 삭제한 버전을 별도로 첨부해 놓았으니 이쪽을 이용해서 빌드해 주세요. (scp로 업로드해서 실행확인했습니다)


