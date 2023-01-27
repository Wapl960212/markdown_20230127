# markdown_20230127
마크다운 설명

### 11. 표
|번호|아이디|이름|레벨|이메일|등록일|
|:----|:----|:----|:----|:----|:----|
|1|good|나야|naver|20220127|2020|
|2|good|나야|naver|20220127|2020|
|3|good|나야|naver|20220127|2020|
|4|good|나야|naver|20220127|2020|
|5|good|나야|naver|20220127|2020|

### 10. 인라인
문단 중간에 'CODE'를 넣을 수 있습니다.(고정형 폭 폰트를 ㅅ표시해야할떄 사용)
예를 들어 'print('question_id:{}'.format(question_id))' 처럼


### 9. 강조
**Spring**을 만긱하세요
__*Spring*__을 만긱하세요

### 8. 이미지 넣기
![팽귄](https://github.com/Wapl960212/markdown_20230127/blob/main/%ED%8C%BD%EA%B7%84.png)


### 7.하이퍼 링크
[네이버](https://naver.com)

### 6.가로 라인
---
***

### 5. 코드블록
'''
def detail(request,question_id):

    print('question_id:{}'.format(question_id))
    #question=Question.objects.get(id=question_id)
    question = get_object_or_404(Question,pk=question_id)
    print('2.question:{}'.format(question))
    context = {'question':question}
    return render(request,'pybo/question_detail.html',context)



def index(request):
    print('index 에벨로출력')
    question_list= Question.objects.order_by('-create_date')

    context = {'question_list':question_list}
    return render(request,'pybo/question_list.html',context)
'''

### 4. 목록
1. 아이템1
2. 아이템2
  9. 단계 하위 아이템
    3. 단계 하위 아이템
9. 아이템3
  
- 아이템 1
+ 아이템 2
  - 1단계 하위
    * 2단게 하위

순서없는 목록
* 목록이름
* 목록
* 목록

순서가 있는 목록   
1. 목록이름
2. 목록
3. 목록3번

### 3. 인용문
> 여기에 인용할 내용을 넣으면 됩니다.
> 빈줄이 없으면 자동으로 인용 상자에 포함이 됩니다.

### 2. 헤더
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5

### 1. 문단 구문을 위한 개행.
문단을 작성 합니다.   (개행 공백 두개)
겨울이 가고 봄이 옵니다.
