# 게임 프로젝트

## 목차
 1) [게임 소개](#게임-소개)

 2) [게임 개발 환경](#게임-개발-환경)

 3) [주차별 실행 현황](#주차별-실행-현황)

 4) [게임 관련 아이템과 함정 및 발판](#게임-관련-아이템과-함정-및-발판)

 5) [미 구현과 추가 구현 설명](#미-구현과-추가-구현-설명)
 
 6) [주차별 계획](#주차별-계획)    
 
<hr>

### 게임 소개
 게임 이름: Run Slime

 게임 장르: 플랫포머, 퍼즐

 플랫포머: 점프와 이동기를 사용하는 게임을 말한다. 플랫폼이란 발판을 의미하는데 구체적으로 플레이어가 
       캐릭터를 조종하면서 발판 위를 뛰어다니는 점프 컨트롤이 중요한 게임이다.

 퍼즐: 어떠한 규칙 내에서 정해진 행위를 통해 주어진 조건을 완료해 클리어하는 단순한 게임을 지칭한다. 
       게임의 특성상 변수가 전혀 없거나 극히 드물다는 특성이 있다.

 스토리: 슬라임의 무리에서 떨어져버린 슬라임이 자신의 둥지를 찾아 여행을 하는 이야기

#### 플레이 방법:

  1. 이동기 점프(W), 좌우 이동키(A, D)를 이용하여 플레이어 자신을 이동시킨다.

  2. 아이템을 먹고 마우스 좌클릭과, 우클릭를 이용한다.

  3. Space키는 특수키로 이동하는 방향으로 짧게 대쉬를 한다.

  4. 여러 개의 장애물을 피하면서 여럿 문제를 풀어서 목표 지점으로 간다.

  5. 하나믜 맵으로 이루어져 있는 것이 아닌 여러 개의 맵(스테이지)가 있어 여러 맵을 플레이 할 수 있다.

#### 에셋 소개(출처):
  ● 타일맵에 사용 할 에셋 (FREE Pixel Art kit)      
       사이트: https://assetstore.unity.com/
     
  ● 아이템으로 사용 할 에셋 (Jelly Icons)    
       사이트: https://assetstore.unity.com/
     
  ● 플레이어로 사용 할 에셋 (2D Pixel Slime Set)    
       사이트: https://www.gamedevmarket.net/category/2d/
     
  ● 플레이어 대쉬 사운드    
       사이트: https://www.sellbuymusic.com/
     
  ● 배경 음악, 아이템 효과 사운드    
       사이트: https://pixabay.com/ko/sound-effects/

<hr>

### 게임 개발 환경

 개발할 엔진: 유니티
 2D 게임 제작이 처음이더라도 다양한 툴을 자유롭게 사용할 수 있고 2D 게임 제작에 중요한 기능의 대부분은 즉시 사용할 수 있거나
 에디터 창에서 쉽게 설치할 수 있기 때문

 게임 관련 에셋: 유니티 에셋 스토어
 여러 종류의 에셋을 무료와 유로로 구매하여 사운드와 이미지파일을 이용하여 게임 에셋을 구할 예정
 원하는 사운드 파일이 없을 경우 freesound.org 같은 저작권 없고 무료로 제공하는 사이트에서 자신에게 맞는 사운드를 사용할 예정

 사용할 언어: 유니티가 기본적으로 C#을 제공하기 때문에 C#을 이용하여 사용함

<hr>

### 주차별 실행 현황

#### 1주차
##### 1) 게임 계획서 작성    
유니티와 언리얼엔진에서 한 가지를 생각하여 자신이 원하는 게임을 만들기 적합한지 알아보고
어떤 장르의 게임을 개발 할지와 모티브, 방법, 개발 환경을 생각한 다음
PPT와 깃허브를 이용하여 게임 개발과 관련된 정보를 정리하였음

#### 2주차
##### 1) 플레이어 이동    
플레이어가 점프키인 W와 좌우 이동키인 A,D를 이용하여 이동하는 것을 구현
![슬라임 움직임과 점프 구현-min](https://user-images.githubusercontent.com/101154683/164979952-f664191d-e3aa-4ec3-b2cc-1b517d17af87.gif)

##### 2) 긴 점프와 짧은 점프    
플레이어가 점프인 W키를 누르면 점프를 하는데    
점프를 살짝 누를 때와 길게 누를 때의 중력 크기를 다르게 하여 구현
![슬라임 낮은 점프와 높은 점프-min](https://user-images.githubusercontent.com/101154683/164979927-4f15dda7-818e-4e11-a2f1-e90694ec944a.gif)

#### 3) 타일맵 추가 후 플레이아와 충돌 처리    
여러개의 타일을 그린 후 플레이어가 해당하는 타일에 충돌시 이동을 하지 못하도록 구현

#### 3주차

##### 1) 플레이어가 움직일때의 애니메이션 추가    
플레이어가 정지하거나 좌우로 이동할때, 점프할 때의 애니메이션을 구현
![슬라임 애니메이션 구현-min](https://user-images.githubusercontent.com/101154683/164979940-3b053033-cbc1-49dd-a11f-5ad1d2fb3b81.gif)

##### 2) 플레이어의 특수키(대쉬)를 구현    
플레이어가 스페이스 바를 누를시 현재 가고 있는 방향으로 대쉬 하는것을 구현
![슬라임 대쉬 구현-min](https://user-images.githubusercontent.com/101154683/164979931-5bf9181d-4c65-4a6f-b58e-6107e3aa4239.gif)

#### 4주차

##### 1) 플레이어가 가시에 충돌 시 뒤로 넉백    
플레이어가 가시에 충돌을 한다면 현재 가고 있는 방향의 반대 방향으로 이동을 하며    
그 동안에는 플레이어가 대쉬나 이동 및 아이템을 사용하지 못하도록 구현    
![슬라임 가시 충돌 넉백 구현-min](https://user-images.githubusercontent.com/101154683/164979925-23d37d32-013c-4e0e-9331-f2a22506a405.gif)

##### 2) 특수 키(대쉬)를 사용 한 후 딜레이를 알리는 UI    
플레이어가 특수 키(대쉬)를 사용을 하면 플레이어의 위에 딜레이 바를 구현    
자신의 특수 키의 재사용하기 까지의 가시성을 부여하였음

##### 3) 아이템 상자 ( 점프 1회 추가)    
플레이어가 해당하는 아이템 상자를 획득(충돌)을 한다면 점프 횟수를 1번 증가시키게 구현    
하지만 아이템 획득 후 바닥과 충돌을 한다면 획득한 후의 점프 횟수는 초기화 됨
![슬라임 아이템 상자 1회성 점프 추가 구현-min](https://user-images.githubusercontent.com/101154683/164979933-406a522c-b98f-4e62-a44b-ed95a792a0bb.gif)

#### 5주차

##### 1) 아이템 상자 스포너    
플레이어가 아이템 상자를 획득 해도 다시 아이템 상자가 생성될 수 있도록 구현    
![아이템 상자 스포너 구현-min](https://user-images.githubusercontent.com/101154683/164979963-5d203e75-8e5d-40cb-a5ca-af3b60c4ac87.gif)    
추가 구현 필요: [1번 설명](#미-구현과-추가-구현-설명)

##### 2) 아이템 상자 ( 순간 이동 )    
플레이어가 해당 하는 아이템을 획득 하면 자기 중심으로 8방향으로 순간이동을 하도록 구현      
![순간 이동 아이템 구현-min](https://user-images.githubusercontent.com/101154683/164979920-146ad286-091a-4440-b93d-1a157a109765.gif)

##### 3) 플레이어가 열쇠를 획득 후 문과 충돌    
플레이어가 처음에는 문과 충돌을 하면 문과 부딪혀 이동을 할 수 없지만     
열쇠를 획득한 후 다시 문과 충돌을 하면 문이 사라지면서 이동을 할 수 있게 구현
![슬라임 열쇠 획득 후 문 삭제 구현-min](https://user-images.githubusercontent.com/101154683/164979949-1f2c0bf6-2108-48a6-922b-65838579101e.gif)

##### 4) 플레이어가 폭포와 물에 닿으면 이동속도 감소    
플레이어가 해당하는 물에 충돌시 이동속도 감소 구현      
미구현: [2번 설명](#미-구현과-추가-구현-설명)

#### 6주차

##### 1) 배경음악, 대쉬 사운드    
게임을 시작하면 바로 실행이 되며 무한으로 반복하는 배경음악을 설정     
플레이어가 특수 키(대쉬)를 사용하면 나오는 사운드 설정    
사운드는 인 게임안에서 확인하기

##### 2) 플레이어의 좌우 이동시 파티클 추가
플레이어가 좌우로 이동할 시 슬라임의 뒷바닥에 달리는 듯한 파티클을 구현
![슬라임 움직일 때 파티클 구현-min](https://user-images.githubusercontent.com/101154683/164979951-1bfeea47-9f16-4f92-91f5-013b15892492.gif)    

##### 3) 움직이는 발판
플레이어가 올라탈수 있고 다른 장소로 이동하기 위해 사용하는 발판 구현    
![움직이는 발판 구현-min](https://user-images.githubusercontent.com/101154683/164979967-245495e3-7e16-425d-b920-6d4b371441ec.gif)      
추가 구현 필요: [3번 설명](#미-구현과-추가-구현-설명)

#### 7주차

##### 1) 갈고리 이동    
플레이어가 좌클릭 시 갈고리에 맞는 Tag에 충돌시 갈고리가 걸려 플레이어가     
그 방향을 중심으로 U자로 이동 구현    
![갈고리 구현-min](https://user-images.githubusercontent.com/101154683/164983824-c52d0a21-ebfa-43c7-b2c6-1a91f2f0e9df.gif)    

##### 2) 아이템 상자 ( 갈고리 )    
플레이어가 해당 아이템 획득 시 갈고리를 1회 사용 가능하도록 구현    
추가 구현 필요: [4번 설명](#미-구현과-추가-구현-설명)

#### 8주차

##### 1) 플레이어와 발판 이동처리
6주차에서 움직이는 발판 미구현 사항을 구현함으로써 플레이어가 발판에 착지했을때 발판과 플레이어가 같은 속도로 움직이게 구현    
![플레이어와 발판 x축 이동처리-min](https://user-images.githubusercontent.com/101154683/174471507-ab001f03-b73f-490d-9622-0d331d2c6e69.gif)

##### 2) 갈고리 아이템 추가와 1회 사용으로 구현
7주차에서 갈고리 아이템 사용하는 것 까지는 구현을 하였지만 갈고기 아이템을 쓰기위한 상자를 만들지 않아 이어서 구현하였음    
![갈고리 아이템 추가와 1회 사용으로 구현-min](https://user-images.githubusercontent.com/101154683/174471528-e60d283d-557c-4e22-9442-72653a5b3bf5.gif)

##### 3) 아이템 스포너에 중복되지 않게 스폰 변경
플레이어가 아이템 상자를 획득했을 때 스폰을 개별이 아닌 단체로 지정을 하여 먹지도 않은    
아이템 상자가 스폰하는 문제가 발생하였는데 그 문제를 해결하기 위한 구현    
![아이템 스포너에 중복되지 않게 스폰 변경-min](https://user-images.githubusercontent.com/101154683/174471544-4de20e22-2fcc-4322-936c-8364d5c96e7d.gif)

#### 9주차

##### 1) 플레이어와 물에 접촉 시 이동속도 감소 및 중력값 설정
5주차에서 물에 접촉시 이동속도와 중력값을 바뀌게 하는 것을 못하였는데 이번 주차에 구현하였음    
![플레이어와 물 접촉 이동 감소-min](https://user-images.githubusercontent.com/101154683/174471567-b04a0c26-dfc2-4b7b-80c3-795cc22ea480.gif)

##### 2) 타일맵 충돌 추가 처리
플레이어가 순간이동 시 타일맵에 끼거나 플레이어가 빠른 속도로 떨어질때 벽에 끼거나 통과되는 문제가 발생하였는데 수정하였음    

##### 3) 인게임 씬에서 마우스 커서 변경
인게임 씬에서 원래의 마우스 커서가 아닌 다른 커서를 사용하였음    
![인게임 마우스커서](https://user-images.githubusercontent.com/101154683/174473343-c775dc2b-b7d6-49c9-9ed2-94377f82a373.png)
    

#### 10주차

##### 1) 플레이어가 순간이동 후 중력 수치 설정
플레이어가 떨어지는 도중 순간이동을 할 시 중력값이 그대로 이어져 부자연스럽게 떨어지는것을 고침    

##### 2) 아이템획득과 열쇠를 얻는것을 알리는 UI 구현
플레이어가 열쇠와 아이템을 획득시 시각적으로 알 수 있게 UI를 구현    
![아이템과 열쇠를 얻으면 알수있게 UI구현](https://user-images.githubusercontent.com/101154683/174471674-bf391a28-f633-4e7f-a7cd-394a2055f20b.gif)

#### 11주차

##### 1) 인트로씬 구현 (시작버튼 구현)
인게임씬으로 넘어가기 전에 있을 씬으로 시작버튼을 구현하여 버튼 클릭시 메인 씬으로 넘어가게 구현    
![인트로씬 구현-min](https://user-images.githubusercontent.com/101154683/174472079-d02fd18d-fdfd-4057-b031-20b7a58e76f9.gif)

##### 2) 인게임씬에서 12시 방향에 메뉴창 구현 및 게임 재시작과 종료, 취소 버튼 구현
인게임 중 12시 방향에 톱니바퀴를 클릭시 종료와 재시작, 취소 버튼이 나오게하여    
클릭시 게임을 재시작하거나 종료 또는 메뉴창을 닫힐수 있게 구현    
![인게임씬 메뉴창 구현-min](https://user-images.githubusercontent.com/101154683/174472096-99ce483e-29ae-4e1b-ac50-159e0d212159.gif)

##### 3) 아이템, 열쇠 획득 시 사운드 구현
플레이어가 아이템과 열쇠를 획득 할 시 사운드 구현    
사운드는 인 게임안에서 확인하기

##### 4) 플레이어가 문 충돌시 열쇠 여부에 따른 사운드 구현
플레이어가 열쇠의 여부에 따라 문 충돌시 사운드가 다르게 구현    
사운드는 인 게임안에서 확인하기

#### 12주차

##### 1) 인게임씬에서 종료와 재시작 버튼을 누를시 한번 더 물어보게 구현
메뉴창에서 종료와 재시작 버튼을 누를시 바로 실행을 하지 않고 한번 더 물어보고 실행하게 구현    
![인게임씬 메뉴창 한번더 물어보게 구현-min](https://user-images.githubusercontent.com/101154683/174472110-a693e3c8-2a1c-48f2-9989-7ea2623db251.gif)

##### 2) 인트로씬 추가로 꾸미기(종료 버튼, 배경음악 등 여러가지 구현)
인트로 씬에 추가로 종료 버튼과, 배경음악과 버튼 클릭시 사운드 구현    
![인트로씬 추가로 구현-min](https://user-images.githubusercontent.com/101154683/174472133-6171da25-6147-492a-a85b-e93acb163c52.gif)

##### 3) 아이템 사용시 사운드 구현    
워프 아이템과 갈고리 아이템을 사용할 때 사운드 구현    
사운드는 인 게임안에서 확인하기    

##### 4) 메뉴 창 누를시 배경음악 및 게임 정지 구현    
메뉴 창을 누르면 배경음악이 정지되며 플레이를 하지 못하게 시간을 정지시키게 구현    
사운드는 인 게임안에서 확인하기    

#### 13주차

##### 1) 메인 스테이지 제작
처음 샘플 맵에서 새롭게 스테이지를 만들어 메인 씬으로 제작
튜토리얼 스테이지:    
![튜토리얼스테이지](https://user-images.githubusercontent.com/101154683/174473640-a75aec7d-181d-4f4b-83f4-ca7be5c16893.png)    
1스테이지:    
![스테이지1](https://user-images.githubusercontent.com/101154683/174473639-ef99502a-657f-4c70-b246-767bc4605b5a.png)    
2스테이지:    
![스테이지2](https://user-images.githubusercontent.com/101154683/174473660-189c2507-cd24-4924-b769-5ef4e129c9ea.png)    

##### 2) 인트로씬 마우스 커서 변경
게임 시작할 때의 마우스 커서의 모양을 바꾸게 구현    
![인트로 마우스커서](https://user-images.githubusercontent.com/101154683/174472154-0d9600ab-f247-4905-a9da-8d3c3df0c065.png)

#### 14주차

##### 1) 메인 스테이지 추가 제작 
제작 중인 메인 씬을 추가로 제작    
3스테이지:    
![스테이지3](https://user-images.githubusercontent.com/101154683/174473658-505a26cc-b9ec-42aa-83c1-cfb32de186a0.png)

##### 2) 인트로 씬 추가 구현 
인트로 씬에서 움직이는 영상을 보여주면서 점점 흰색으로 바뀌며 버튼이 나오게 구현    
![인트로씬 추가 구현(영상추가)-min](https://user-images.githubusercontent.com/101154683/174472181-8ee95591-d75c-47b8-ab04-c0264aa9f7c0.gif)

##### 3) 엔딩 씬 추가와 꾸미기
플레이어가 마지막 목표 지점에 도착하면 엔딩 씬으로 이동하게 구현과 엔딩 씬 Text추가    
![엔딩 씬 추가와 추가 구현](https://user-images.githubusercontent.com/101154683/174472192-8ffa2e3e-c780-4d93-96e5-df6d546ddca8.gif)

#### 15주차

##### 1) 인게임씬에서 재시작 마다 세이브 위치 구현
플레이어가 스테이지 별로 메뉴창에서 재시작 버튼을 눌렀을 때 스테이지의 처음 부분으로 다시 시작할 수 있게 구현    
1스테이지:     
![1스테이지 재시작-min](https://user-images.githubusercontent.com/101154683/174471137-e2bd5742-d0d0-4074-a048-11cd0720bc8f.gif)    
2스테이지:     
![2스테이지 재시작-min](https://user-images.githubusercontent.com/101154683/174471145-d717ff8c-6948-415f-83b6-4405e59b3077.gif)    
3스테이지:     
![3스테이지 재시작-min](https://user-images.githubusercontent.com/101154683/174471142-413f26c2-9a37-4129-934f-364f94de388f.gif)    

##### 2) 스테이지마다 배경음악 다르게 구현
스테이지가 튜토리얼 스테이지 포함 4개가 있는데 플레이어가 스테이지안의 좌표에 있을 때 배경음악이 바뀌게 구현     
사운드는 인 게임안에서 확인하기 

##### 3) 엔딩 씬에 다시 시작과 종료 버튼 구현
엔딩 씬에서 다시 시작할 것인지 종료 할것인지를 선택하는 버튼을 구현     
![엔딩씬 버튼-min](https://user-images.githubusercontent.com/101154683/174490491-3964896e-116b-4d20-8c8a-00a93b89b462.gif) 

<hr>

### 게임 관련 아이템과 함정 및 발판

#### 1) 아이템
● 점프 아이템: 점프의 횟수를 1회 더 늘려준다. (바닥에 착지하면 횟수는 사라진다.)     
![점프 1회](https://user-images.githubusercontent.com/101154683/164984545-5734f6d6-b618-4079-b67c-c8ea3f1eaecb.png)
    
● 순간이동 아이템: 자신을 기준으로 8방향에서 원하는 위치로 순간이동이 가능하다.     
![순간이동](https://user-images.githubusercontent.com/101154683/164984542-ca872bb5-26c3-4f5d-80ec-8e71a1baa6ea.png)
    
● 갈고리 아이템: 자신의 마우스 기준으로 플레이어가 갈고기를 걸어 이동할 수 있다.    
![갈고리아이템](https://user-images.githubusercontent.com/101154683/174472911-95be0d10-0da8-45e5-b37c-9c043790e6ef.png)
    
● 열쇠: 문으로 인해 가지 못하는 구간을 열수 있다.     
![열쇠](https://user-images.githubusercontent.com/101154683/164984543-7b34637d-54b3-4d45-8dae-6faef93d5d7e.png)

● 문: 열쇠를 가지고 있어야 다음 스테이지로 갈 수 있다.    
![문](https://user-images.githubusercontent.com/101154683/174472977-e05ce302-68f3-4a64-9e9c-c735989d41ac.png)

#### 2) 함정 및 발판
● 가시: 플레이어가 충돌한다면 자신이 가고 있던 방향의 정반대로 넉백하며    
바닥에 착지를 할 동안 아이템 및 이동을 할 수 없다.     
![가시](https://user-images.githubusercontent.com/101154683/164985020-e31e0cac-445a-438f-99f0-1a9efa3a1359.png)
    
● 발판: x축과 y축으로 이동하는 발판으로 가지 못하는 구간을 움직이는 발판으로 이동 할 수 있다.     
![발판1](https://user-images.githubusercontent.com/101154683/164985022-e1022c66-3e4d-4fbc-8b3a-d5df215e0d4d.png)  ![발판2](https://user-images.githubusercontent.com/101154683/164985023-b062222d-0f43-403b-a28e-68212d311f8f.png)
    
● 깃발: 슬라임의 둥지에 있으며 자신(슬라임)이 해당 아이템에 충돌시 엔딩 씬으로 넘어가게 된다.    
![엔딩지점](https://user-images.githubusercontent.com/101154683/174474479-d39468b8-4693-407c-bfbc-5bc5e1a5ca3e.png)

<hr>

### 미 구현과 추가 구현 설명

#### 1번 설명: 아이템을 획득하는 것와 관계없이 아이템이 지속적으로 스폰이 되는 현상을 수정하지 못하였음
해결 방안: 아이템 스포너를 생성하여 해당 스포너의 아이템을 획득하면 5초 후에 생성하게 할 예정 [21.04.06 수정 완료]

#### 2번 설명: 해당 물이 애니메이션 타일로 콜라이더를 추가하지 못하여 구현을 하지 못함
해결 방안: 해당 물 타일에 투명의 오브젝트를 추가하여 is Trigger를 사용하여 충돌 처리를 사용할 예정 [21.04.27 수정 완료]

#### 3번 설명: 구현 하지 못함 플레이어가 발판에 착지를 하여 가만히 있을 때 발판과 플레이어와의 속도를 같게 하지 못하였음    
해결 방안: 충돌 처리를 이용하여 발판의 속도를 플레이어의 속도와 합칠 예정 [21.04.20 수정 완료]

#### 4번 설명: 그 기간에는 중간고사로 구현을 하지 못함
해결 방안: 다음 기간에 할 예정

<hr>

### 주차별 계획 
#### (주차별 실행 현황에 자세히 있으므로 간략하게 생략하였음)

21.03.02: 게임프로젝트 계획서 작성

21.03.09: 플레이어 이동 구현, 길고 짧은 점프 구현, 타일맵 추가 후 충돌 처리

21.03.16: 플레이어 애니메이션 추가, 대쉬 키 구현

21.03.23: 가시 구현, 대쉬 딜레이 UI 구현, 점프 1회 아이템 구현

21.03.30: 아이템 스포너 구현, 순간이동 아이템 구현, 문과 열쇠 구현

21.04.06: 배경음악과 대쉬 사운드 구현, 이동 파티클 구현, 발판 구현

21.04.13: 갈고리 구현, 갈고리 아이템 구현

21.04.20: 플레이어 발판 이동처리, 갈고리 아이템 획득 시 1회만 사용 가능하게 구현

21.04.27: 플레이어가 물의 접촉시 이동속도 및 중력 값 설정, 타일맵 충돌 추가 처리, 인게임씬 마우스 커서변경

21.05.03: 순간이동 후 중력 수치 설정, 아이템과 열쇠를 획득 시 알려주는 UI 구현

21.05.10: 게임 인트로씬 구현(스타트 버튼 누를시 인게임으로 이동하게 구현), 인게임씬에서 12시 방향에 메뉴창(재시작, 종료, 취소) 구현
        아이템, 열쇠 획득 시 사운드, 열쇠 획득 했을때와 안했을 때의 사운드 구현

21.05.17: 인게임씬에서 종료와 재시작 누를시 한번 더 물어보게 구현, 인트로 씬 좀더 구현(시작시 움직이는 이미지 추가 등), 아이템 사용시 사운드 구현
        메뉴 창 눌르시 배경음악과 시간 정지 구현

21.05.24: 메인 스테이지 제작, 인트로 씬 마우스 커서 변경

21.05.31: 메인 스테이지 추가 제작, 인트로 씬 사진 추가, 엔딩 씬 추가와 꾸미기

21.06.07: 메인 스테이지 재시작 마다 세이브 위치, 배경음악 구현, 엔딩 씬에 다시 시작과 종료 버튼 구현

