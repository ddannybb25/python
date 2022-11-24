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
----
>TIL

22.11.24 apply,lambda 

apply,lambda에 대한 공부를 하였고 블로그 정리 완료

https://tadadata.tistory.com/5

22.11.25 파일명[학습 n232 code] 복습

TIL : loc,iloc,인덱스리셋,apply lambda

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
