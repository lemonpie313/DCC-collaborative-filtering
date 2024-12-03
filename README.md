# 2024 데이터 크리에이터 캠프


## 미션 설명

### Mission 1. 패션 스타일 이미지 분류
#### 1-1. 이미지 ID 수 기준 성별&스타일 표 작성
주어진 이미지 데이터의 파일 명은 “{W/T}\_{이미지ID}\_{시대별}\_{스타일별}\_{성별}.jpg” 와 같은 형식이다. 이에 기반하여 “이미지ID” 수 기준으로 “성별 & 스타일” 통계치를 아래 표 형식으로 기입한다.

<table>
    <tr>
    <th>성별</th>
    <th>스타일</th>
    <th>이미지 수</th>
  </tr>
  <tr>
    <th rowspan="4">여성</th>
    <td>feminine</td>
    <td></td>
  </tr>
  <tr>
    <td>classic</td>
    <td></td>
  </tr>
  <tr>
    <td>minimal</td>
    <td></td>
  </tr>
  <tr>
    <td>...</td>
    <td></td>
  </tr>
<tr>
    <th rowspan="4">남성</th>
    <td>ivy</td>
    <td></td>
  </tr>
  <tr>
    <td>mods</td>
    <td></td>
  </tr>
  <tr>
    <td>hipple</td>
    <td></td>
  </tr>
  <tr>
    <td>...</td>
    <td></td>
  </tr>
</table>

#### 1-2. 클래스 분류
ResNet-18를 활용하여 "성별 & 스타일" 단위로 클래스 분류를 수행하고, Validation 데이터에 대한 정확도를 제시한다.
- Resnet-18의 parameters는 무작위로 초기화하여 사용한다. (즉, pretrained weights는 사용할 수 없음)
- 성능을 높이기 위해 object detection, image cropping 등의 다양한 데이터 전처리 기법을 활용해도 무방하다. (데이터 전처리 단계에 한해서는 외부 라이브러리 활용 가능)

### Mission 2. 패션 스타일 선호 여부 예측
#### 2-1. 설문 ID 수 기준 성별&스타일 표 작성
주어진 라벨링 데이터의 파일 명은 “{W/T}\_{이미지ID}\_{시대별}\_{스타일별}\_{성별}\_{설문ID}.json” 와 같은 형식이다. 이에 기반하여 “설문ID” 수 기준으로 “성별 & 스타일” 통계치를 아래 표 형식으로 기입한다.

<table>
    <tr>
    <th>성별</th>
    <th>스타일</th>
    <th>이미지 수</th>
  </tr>
  <tr>
    <th rowspan="4">여성</th>
    <td>feminine</td>
    <td></td>
  </tr>
  <tr>
    <td>classic</td>
    <td></td>
  </tr>
  <tr>
    <td>minimal</td>
    <td></td>
  </tr>
  <tr>
    <td>...</td>
    <td></td>
  </tr>
<tr>
    <th rowspan="4">남성</th>
    <td>ivy</td>
    <td></td>
  </tr>
  <tr>
    <td>mods</td>
    <td></td>
  </tr>
  <tr>
    <td>hipple</td>
    <td></td>
  </tr>
  <tr>
    <td>...</td>
    <td></td>
  </tr>
</table>

#### 2-2. 
2-1에서 구한 유효한 라벨링 데이터만 따로 분리하여 아래와 같이 100명 응답자의 "스타일 선호 정보표"를 구한다. 파일은 json 포맷으로 되어 있으며 json 필드 중, "응답자 ID"는 "user>R_ID"로 알 수 있고, "스타일 선호 여부"는 "item>survey>Q5"로 알 수 있다. 스타일 선호도 값은 "1:비선호", "2:선호"이다.

<table border="1" style="border-collapse: collapse; text-align: center;">
  <tr>
    <th rowspan="2">응답자 ID</th>
    <th colspan="2">Training</th>
    <th colspan="2">Validation</th>
  </tr>
  <tr>
    <th>스타일 선호</th>
    <th>스타일 비선호</th>
    <th>스타일 선호</th>
    <th>스타일 비선호</th>
  </tr>
  <tr>
    <td rowspan="2">64747</td>
    <td>W_07894_00_cityglam_W.jpg</td>
    <td>W_44386_80_powersuit_W.jpg</td>
    <td>W_05628_00_cityglam_W</td>
    <td>W_34024_10_sportivecasual_W.jpg</td>
  </tr>
  <tr>
    <td>W_37160_70_punk_W.jpg</td>
    <td>W_34573_10_sportivecasual_W.jpg</td>
    <td></td>
    <td></td>
  </tr>
</table>





## 실행 방법

## 
