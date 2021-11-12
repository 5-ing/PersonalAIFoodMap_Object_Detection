# 뭐먹었지도 | Personal AI FoodMap
<p>&nbsp;본 프로젝트는 2021년 1,2학기 '캡스톤디자인' 수업을 통해 진행한 프로젝트입니다. </p>

## 프로젝트 소개
<p>&nbsp;팀원들 모두 지인들에게 식당을 추천할 때, 자신이 갔을 때의 사진을 보며 설명해야하는 경험을 종종 겪어 왔습니다. <br>
하지만 갤러리의 수많은 사진들 중에서 음식 사진만을 추려내는 것은 쉽지 않은 과정이었고, <br>
이 중에서도 '어디서 뭘 먹었는지' 떠올리는 것은 더 어려운 일이었습니다. </p>

<p>&nbsp;이러한 일상 속 어려움에서 아이디어를 고안해 갤러리에서 음식 사진만을 찾아 지도상에 표시해주고 <br>
식당을 찾아주는 '뭐먹었지도'를 개발하게 되었습니다.</p> 

## 진행 기간
2021년 3월 ~ 2021년 11월

## 팀원들
<table align="center" border="1.5" bordercolor="gray">
    <tr>
        <td align="center"><a href="https://github.com/Ryeoryeon"><img src="https://avatars3.githubusercontent.com/u/50348995?s=500&u=7484588e133e5efa66f6cd14dac2417a90a4f598&v=4" width="180px;" alt=""/><br/><sub><b>이영현()</b></sub></a></td>
        <td align="center"><a href="https://github.com/jinjinzara"><img src="https://avatars.githubusercontent.com/u/82082271?v=4" width="180px;" alt=""/><br/><sub><b>진소연()</b></sub></a></td>
        <td align="center"><a href="https://github.com/gemiJ"><img src="https://avatars.githubusercontent.com/u/30407907?v=4" width="180px;" alt=""/><br/><sub><b>주윤겸()</b></sub></a></td>
    </tr>
</table>

## 모델 훈련
<p>YOLOv3 모델, UEC-FOOD256 데이터 사용 <br>
Darknet 환경에서 훈련 <br> <br>
사용한 주요 명령어 </p>
Test local images <br>

```
darknet.exe detector test food/food256.data cfg/yolov3-tiny-food.cfg food/backup/yolov3-tiny-food_last.weights -i 0
``` 

Train from checkpoint

```
darknet.exe detector train food/food256.data cfg/yolov3-tiny-food.cfg food/backup/yolov3-tiny-food_last.weights
```
