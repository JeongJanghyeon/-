# -import random

print("▽▼"*9)
print("안녕하세요 장현이네 로또상점입니다.")
print("△▲"*9)

while True:
    money=int(input("\n얼마 구매하시겠습니까? (상점을 나가시려면 0입력): "))
    print("\n")
    finish=money//1000
    if money%1000==0:

      for i in range(finish):
        lotto=random.sample(range(1,46),6)
        lotto.sort()
        print("{0:>2} LOTTO: {1}".format(i+1,lotto))
        if(i+1)==5:
            print("-"*40)

    else:
        print("천원 단위로 지불해주세요. ")
        

    if money==0:
        break
