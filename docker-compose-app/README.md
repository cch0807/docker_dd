# 레디스란 ?
- Redis(REmote Dictionary Server)는 메모리 기반의 키-값 구조 데이터 관리 시스템이며, 모든 데이터를 메모리에 저장하고 빠르게 조회할 수 있는 비관계형 데이터베이스(NoSql)이다.

# 레디스를 쓰는 이유 ?
- 메모리에 저장을 하기 때문에 Mysql같은 데이터베이스에 데이터를 저장하는 것과 데이터를 불러올 때 훨씬 빠르게 처리할 수 있으며, 비록 메모리에 저장하지만 영속적으로도 보관이 가능하다. 그래서 서버를 재부팅해도 데이터를 유지할 수 있는 장점이 있다.

# Node.js 환경에서 Redis 사용 방법
- 우선 redis-server 작동.
- redis 모듈 다운받기.
- 레디스 모듈을 받은 후 레디스 클라이언트를 생성하기 위해서 Redis에서 제공하는 createClient() 함수를 이용해서 redis.createClient로 레디스 클라이언트를 생성한다.

# 도커 환경에서 레디스 클라이언트 생성 시 주의사항
- 보통 도커를 사용하지 않는 환경에서는 Redis 서버가 작동되고 있는 곳의 host 옵션을
URL로 위에 처럼 주면 되지만, 도커 Compose를 사용할 때는 host 옵션을 docker-compose.yml 파일에 명시한 컨테이너 이름을 주면된다.

# yml이 뭘까..
- YAML ain't markup language 약자이며, 일반적으로 구성 파일 및 데이터가 저장되거나 전송되는 응용 프로그램에서 사용되고 원래는 XML이나 json 포맷으로 많이 쓰였지만, 좀 더 사람이 읽기 쉬운 포맷으로 나타난게 yaml이다.

# docker-compose up vs docker-compose up --build
- docker-compose up 이미지가 없을 때 이미지를 빌드하고 컨테이너 시작
- docker-compose up --build 이미지가 있든 없든 이미지를 빌드하고 컨테이너 시작