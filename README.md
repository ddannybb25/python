# python 기초를 탄탄하게, 반복만이 살 길이다 

# TIL(Today I learned) 1일 1커밋 

  부트캠프 수업 시작 전 6시-7시 30분 파이썬기초를 다져보는 시간

----
>배우고자 하는 개념

- [ ]  groupby, get_groupby(n232)

https://celltong.tistory.com/entry/%ED%8C%8C%EC%9D%B4%EC%8D%AC-pandas-groupby-%ED%95%A8%EC%88%98%EB%A1%9C-%EA%B7%B8%EB%A3%B9%EC%9C%BC%EB%A1%9C-%EB%AC%B6%EA%B8%B0

- [ ]  merge (n232)
- [ ]  df.query에서 groupby, get_groupby (n232a)
- [ ]  수업시간 코딩 파일 (특히 merge index부분 잘보기), 파일명 학습 n232code
- [ ]  concat 
- [ ]  str,~
- [ ]  정규표현식
- [ ]  ZIP N234 
- [ ]  feature engineering -> 이거 꼭!! 안그러면 계속 막힐 것(n213부터 나옴)
- [ ]  파이썬 머신러닝 완벽가이드, 캐글 필사 
```
pdp = pdp.rename(columns=dict(zip(category_codes, category_names)))
```

----
>TIL


[22.11.24 apply,lambda ]

apply,lambda에 대한 공부를 하였고 블로그 정리 완료

https://tadadata.tistory.com/5


[22.11.25 파일명[학습 n232 code] 복습]

**TIL : loc,iloc,인덱스리셋,apply lambda**

더 공부하고 싶은 부분 : ~(제외시키는 것),str, all,concat

```
#loc과 iloc의 차이점

students.loc[36698] # 이름으로 '내가'지정

students.iloc[0] # i, index로 지정, 컴퓨터가 알아들을 수 있도록

```

```
#인덱스 리셋

st_new= students.reset_index()

```

```
#merge index 지정해주고 싶을때 

students.merge(score,left_index=True,right_index=True) #인덱스 사용

st_new.merge(score,left_on='id,right_index=True) #새로운 인덱스가 생겨버림

```

```
#apply lambda

students['email'].apply(lambda x :x.split('@')[-1]=='gmail.com')

```

```
#apply

students['email'].apply(is_gmail)
```

```
# ~, str

# ~는 제외시켜라 
base_result=s[~s.question.str.startswith('challenge')]

```

```
#all()

base_correct=base_result.groupby('id').all()['is_correct']

```

[22.11.28]

학습 n232 code 파일 복습

어느정도 학습이 된 것 같으니

내일은 정규표현식 공부하기

```
base_result = s[~s.question.str.startswith('challenge')] 
base_result.reset_index(inplace=True)
base_correct = base_result.groupby('id').all()['is_correct']
base_correct

```

[22.11.29]

TIL) **zip** 

n234 zip 

https://www.daleseo.com/python-zip/

```
pdp = pdp.rename(columns=dict(zip(category_codes, category_names)))

```

```
shaps = pd.Series(shap_values[0], zip(feature_names, feature_values))

```

오늘 스챌있으니깐 대략적인 개념 파악하고 다시 복습하기


[22.11.30]

TIL) **df.dropna**

6시 기상, 공부시작 ~ 7시 20분 

어제 스챌 때 feature engineering에 막혀서 

결측치 제거 df.dropna 공부 및 정리 

https://tadadata.tistory.com/6 블로그 정리완료 

오늘부터 프로젝트여서 아침공부를 할 수 있을 지는 모르겠지만 플젝 기록이라도 해두기 

선배기수 블로그보면서 스챌점수보완보다는 나중에 개념 찾아볼 수 있게, 복습,포폴용으로 배운 거 블로그 정리해두기 








