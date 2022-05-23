![header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=170&text=Welcome&desc=Kim's_Work&animation=fadeIn&fontSize=55&fontAlignY=31)

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white)![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white)![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=Kimminseok1122&theme=cobalt)](https://github.com/anuraghazra/github-readme-stats)      [![Solved.acProfile](http://mazassumnida.wtf/api/v2/generate_badge?boj=beggar1122)](https://solved.ac/beggar1122/)

# 프로젝트 제목 : Review System By UX






## 개요
현 코로나 상황에서 많은 여행지의 상황이 바뀌고 기존의 시스템이 역할의 단점을 보완하기 위해 생각한 프로젝트로 사용자 UX를 통해 UI를 구성하고 정보를 제공해주는 플랫폼을 기획하였습니다.


### 본인의 역할
프로젝트의 전반적인 기획과 DB구성 및 조장으로써 역할 분배를 맡았습니다. 또한 네이버 지도API 해석및 응용 과 Ajax검색을 통한 검색기능과 리뷰 등록기능을 구현하였습니다. 아래에서는 제가 구현한 페이지를 보여드리도록 하겠습니다.

### 구현 페이지 및 코드 설명

![image](https://user-images.githubusercontent.com/99003417/169831772-0870d5f9-5c3a-46f8-a8f3-2c8a400befc2.png)

```
1번째 기능은 클릭시에 아래로 이동하면서 숨겨져있던 검색창을 보이게 해주는 버튼입니다. 코드는 다음과 같습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169834731-a97102a9-685b-4a6a-a687-748c952bd581.png)

```
1) 아이콘 클릭시 아래로 이동시켜 주면서 display 속성을 block으로 바꿔주어서 안보이던 화면이 보이게 만들어줍니다.아래는 '맛집탐방' 아이콘을 클릭후 생기는 화면입니다.
```
![image](https://user-images.githubusercontent.com/99003417/169836868-535cb5f2-d756-4ef4-83b9-8db31692c2bd.png)

```
2) 아이콘 클릭시에 Ajax로 전체 리스트를 가져오는 부분입니다. theme의 값을 param으로 넣어주어서 각 테마에 맞는 리뷰들만 결과로 나올 수 있게 만들었습니다. 그 후에 themeArr이라는 배열에 넣어서 data.foreach문 바깥에서 사용 가능 할 수 있도록 하였습니다.
```
```
3) 만약 아이콘 클릭시 이미 검색창이 존재한다면 , 즉 .midcon-box class의 length > 0 다면 empty()로 자식요소를 제거 해주고 새로 검색창을 만드는 기능입니다. 이 과정이 없다면 아이콘을 클릭할 때 마다 계속 리뷰가 쌓일것입니다.
```
![image](https://user-images.githubusercontent.com/99003417/169840364-84dfb5a7-b634-4c67-93c4-ad137230c44a.png)

```
2번째 기능은 클릭시에 아래로 이동하면서 숨겨져있던 유튜브 창을 보여주는 버튼입니다. 코드는 다음과 같습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169840693-0f59e125-b7da-469c-a802-933bf19ba179.png)

```
위 코드 또한 클릭시 자식요소를 검사해 자식요소가 있으면 제거후 유튜브 링크를 자식요소로 추가해주고 없으면 그냥 추가해주는 코드 부분입니다.
```

![image](https://user-images.githubusercontent.com/99003417/169841338-231d4842-f13e-4d76-8332-42c785649d7c.png)
![image](https://user-images.githubusercontent.com/99003417/169841411-5e966db8-7d40-48ca-a231-de437b0a6d9d.png)
![image](https://user-images.githubusercontent.com/99003417/169841485-a528c2e2-4e51-4b23-973b-9eadc674495e.png)

```
main 화면을 구성하는 지도의 주요 세가지 기능을 화면으로 모아보았습니다. 
첫 번째 기능은 클러스터 기능입니다. 클러스트 기능은 일정 화면 줌 Level에 따라 지역의 리뷰 숫자를 나타내는 기능입니다.
코드는 아래와 같습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169842121-c3e19a20-00f7-4caf-a7be-6ada9511caa6.png)
```
클러스터 기능 자체는 네이버API 튜토리얼 측에서 가져온것을 그대로 사용할 수 도 있지만 개인이 수정을 하고자 한다면 두가지를 수정할 수 있습니다. 첫번째는 클러스터 자체의 속성들입니다. 1)번에 나온 속성중에는 maxZoom과 MinCluseterSize 그리고 icons 정도가 개인의 프로젝트에 맞게 수정할수 있는 부분이라고 생각합니다. 2)번에는 리뷰 숫자가 몇개일때 클러스터 이미지가 바뀔것이냐 하는 부분입니다. 각 숫자에 맞게 index를 리턴하여 그 index에 맞는 icon을 표시해 줍니다. 여기서는 count를 몇개를 기준으로 할것인지를 수정할 수 있습니다.
```

![image](https://user-images.githubusercontent.com/99003417/169843167-f017e5d2-c68b-4e58-85b8-e34470782d21.png)

```
다음으로는 마커에 관한것입니다. getLocation 이름의 Ajax controller를 통해서 화면이 로드 될때 정보가 모든 리뷰에 대한 정보가 넘어오고 배열에 담기게 됩니다. 그 다음으로는 그 배열만큼의 for문을 통해 화면에 마커가 나오게 됩니다. (1)번에서는 마커의 속성에 대해서 나오고 있습니다. latlng을 통해 위치를 입력받을 수 있고, marker 안에는 marker의 설정을 어떻게 할것인가에 대해 나오고 있습니다. 여기서 icon을 귀여운 라이온으로 바꾸고 싶으므로 저는 content안에 동적으로 img속성을 주었습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169844482-35d2d792-1dc9-41f9-85b7-dbab618c75ab.png)
```
(2)번째로는 contentString안에 마커안의 내용을 직접 적어줄 수 있습니다. 저는 마커 안에 리뷰 정보가 보이는것이 목표이므로 동적으로 html문과 이벤트를 걸어주어서 각 마커에 맞는 리뷰내용이 나올수 있도록 하였습니다.
```
```
(3)번째로는 마커에 알맞는 리뷰 페이지가 잘 나오는 모습을 확인 할 수 있습니다. 이 페이지는 기존의 리뷰 화면에 지도에 disable과 같은 수정 불가 속성을 넣은것 말고는 차이점이 없으므로 크게 다루지 않도록 하겠습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169845165-1a8fa07b-ba9d-4786-8bb3-ec9b6ae1442a.png)
```
위 화면은 체크박스로 이루어진 Ajax 검색 부분입니다 이 부분에 대한 코드를 보여드리도록 하겠습니다.
```
![image](https://user-images.githubusercontent.com/99003417/169845519-924757c8-a30b-44ea-b6ca-3ff589c48509.png)
```
체크박스에 변화가 생겼을시에 review_groups 배열에 체크된 속성들을 넣어주고 review_theme에 theme값을 입력해 줍니다.  review_groups는 지역에 관한 검색어들이고 review_theme 여행테마 값 입니다.
```
![image](https://user-images.githubusercontent.com/99003417/169846484-c50a0e85-113e-4939-8bf4-29139b605483.png)
```
(1) 위에서 입력받은 review_theme와 review_groups들을 Ajax Controller에서 data를 가져와서 themeArr에 넣어주는 모습입니다.
(2)이 후에 themeArr의 배열길이만큼 리뷰를 생성해서 자식요소로 동적으로 넣어주는 코드입니다.
```

## 프로젝트를 마치면서
프로젝트 초기에 굉장히 힘들었던 부분이 5명의 조원중 2명의 조원의 불참으로 인해 퀄리티와 양에 대한 타협이 많았던 부분이 아쉬웠지만 남아있는 조원 두분이 많이 노력해주었고 제가 최대한 많이 어려운 역할을 맡으려고 노력한 결과 큰 이상없이 마무리 되었습니다. 하지만 지도 API를 더 세심하게 많은 기능을 넣고 싶었던 부분은 조금 아쉬웠습니다.
