# under-fetching
- 클라이언트가 api에 요청을 보냈는데 원하는 데이터를 얻지 못하여 다시 추가적인 api 요청을 보내야 하는 상황.
- 해결 방법 : 
	- 필드 필터링 기능을 통해서 (query-string) 클라이언트가 추가적인 프로퍼티들을 가져 올 수 있게 필터링 기능을 추가한다.
	- `Graphql` 사용.
	- api의 설계를 수정했기 때문에 동시에 클라이언트는 api 요청 코드를 수정된 api 응답 형식에 맞추어 필요한 데이터를 처리하도록 수정 되어야 한다. 비용이 발생함.

# over-fetching
- 해당 under-fetching을 해결 하기 위해서 rest-api에서는 나중에 필요한것 같은 추가적인 프로퍼티들도 반환하게끔 설계를 했을 때 발생하는 문제.
- 클라이언트가 요청한 데이터 이외에 불필요한 정보나 추가적인 프로퍼티들까지 서버에서 반환하는 상황.
- 이로 인해서 네트워크 대역폭이 낭비되고, 클라이언트는 불필요한 리소스를 사용하게 된다.
- 해결 방법 : 
	- 필드 필터링 기능을 통해서 (query-string) 클라이언트가 필요한 필드만 지정하여 요청 할 수 있게 필터링 기능을 추가한다.
	- `Graphql` 사용.
	- api의 설계를 수정했기 때문에 동시에 클라이언트는 api 요청 코드를 수정된 api 응답 형식에 맞추어 필요한 데이터를 처리하도록 수정 되어야 한다. 비용이 발생함.