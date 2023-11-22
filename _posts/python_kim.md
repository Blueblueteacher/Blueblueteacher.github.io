---
layout: post
title: "탕후루 키오스크 만들기"
date: 2023-11-23
excerpt: "#키오스크"
comments: true
---

```python
T = ['딸기','샤인머스캣','귤','블랙 사파이어','파인애플']
T_count = [5, 5, 5, 5, 5]
T_Buy = []
#print('탕후루 종류:',T)

def check(fruit, T_count): # 탕후루 있는지 체크
  if fruit == '딸기':
    if T_count[0] == 0:
      return False
  elif fruit == '샤인머스캣':
    if T_count[1] == 0:
      return False
  elif fruit == '귤':
    if T_count[2] == 0:
      return False
  elif fruit == '블랙 사파이어':
    if T_count[3] == 0:
      return False
  elif fruit == '파인애플':
    if T_count[4] == 0:
      return False
      
cost = 0
success = 0

while True:
  mn = input('메뉴를 입력해주세요(딸기,샤인머스캣,귤,블랙 사파이어,파인애플) 그만 사고 싶으면 X를 입력해주세요 : ')
  if mn == 'X':
    break
  if check(mn, T_count) == False:
    print("탕후루 재고가 없습니다. 결제창으로 넘어갑니다.")
    break
#step2.조건식을 활용하기
  if mn == '딸기':#3000
    cost = cost+3000
    T_count[0] = T_count[0] - 1
    success = 1
    T_Buy.append('딸기')
  elif mn == '샤인머스캣':#3000
    cost = cost+3000
    T_count[1] = T_count[1] - 1
    success = 1
    T_Buy.append('샤인머스캣')
  elif mn == '귤':#3500
    cost = cost+3500
    T_count[2] = T_count[2] - 1
    success = 1
    T_Buy.append('귤')
  elif mn == '블랙 사파이어':#3000
    cost = cost+3000
    T_count[3] = T_count[3] - 1
    success = 1
    T_Buy.append('블랙 사파이어')
  elif mn == '파인애플':#4000
    cost = cost+4000
    T_count[4] = T_count[4] - 1
    success = 1
    T_Buy.append('파인애플')
  else: # 메뉴가 없을 때
    print('해당 메뉴가 없습니다. 결제창으로 넘어갑니다.')
    #print('돈을 돌려드릴게요.'+str(money)+'원')
    break


if success == 1:
  print("구매하신 탕후루는 다음과 같습니다.")
  for i in T_Buy:
    print(i, end=" ")
    print()
  print("결제 금액은 다음과 같습니다")
  print("총 금액 : "+str(cost)+"원")
  money = int(input('돈을 넣어주세요:'))
# 결제
  if money-cost > 0:
    print("탕후루 구매 성공 ! 탕후루와 거스름돈을 가져가세요")
    print("거스름돈 "+str(money-cost)+"원")
  elif money-cost == 0:
    print("탕후루 구매 성공! 탕후루를 가져가세요.")
  else:
    print('돈이 부족합니다.')
    print('부족한 돈'+str(-(money-cost))+'원')
else:
  print("탕후루 구매 실패")
