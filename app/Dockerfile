FROM amazoncorretto:17

# JAR 파일과 entrypoint.sh 파일을 컨테이너의 /app 디렉토리로 복사
COPY studyRecordSecure-0.0.1-SNAPSHOT.jar /app/study.jar
COPY entrypoint.sh /app/entrypoint.sh

# 환경 변수 설정
ENV APP_HOME /app

# 포트 노출
EXPOSE 80

# 볼륨 설정
VOLUME /app/upload

# 작업 디렉토리 설정
WORKDIR $APP_HOME

# entrypoint.sh 실행 권한 부여
RUN chmod +x /app/entrypoint.sh

# 컨테이너 시작 시 실행할 엔트리포인트
ENTRYPOINT ["/app/entrypoint.sh"]