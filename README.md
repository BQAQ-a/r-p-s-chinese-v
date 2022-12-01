#by \/老黑\/
from random import randint
print("石头剪刀布====中文版---rock-paper-scissors--Chinese Version")
wan = input("输入y确认游玩 Do you want to play？y/n")
if wan != "y":
    print("我靠 不玩也得玩！\n")
n = input("告诉我你名字好吧:  ")
t = int(input("你就说你要玩多少把吧: "))
nm = 0
p = 0
c = 0
cnm = 1
print("来吧 " + n + ", 我靠 看我不虐爆你.")
for i in range(t):
    print("========= 积分版 ==============\n\n    回合数: " + str(cnm))
    print("\n-------------------------------\n")
    print(n + ": " + str(p) + " | 老黑: " + str(c))
    cnm += 1
    print("\n===============================\n")
    pl = input("输入 石头 剪刀 或 布: ")
    nnn = 0
    ibm = 99
    while nnn < ibm and pl != "石头" and pl != "布" and pl != "剪刀":
        nnn += 1
        pl = input ("有没有一种可能你输错了 不是说了就只输石头 剪刀 布吗？？？")

    chosen = randint(1,3)
    if(chosen == 1):
      com = '石头'
      comm = 'r'
  
    elif(chosen == 2):
      com = '布'
      comm = 'p'
    else:
      com = '剪刀'
      comm = 's'
    
    print("\n老黑出了: " + com + "\n")
    if(pl == com or comm == pl):
      print('平局')

    elif(pl == "石头" and com == "剪刀"):
      print("玩家 " + n + " 得分！")
      print("\n老黑：卧槽 你是不是开了 你居然赢了")
      p += 1
    elif(pl == "石头" and com == "布"):
      print("老黑得分！")
      print('\n老子赢 哎呀 基本操作')
      c += 1
  
    elif(pl == "布" and com == "石头"):
      print("玩家 " + n + " 得分！")
      print("\n老黑：卧槽 你绝逼开了！ ")
      p += 1
    elif(pl == "布" and com == "剪刀"):
      print("老黑得分！")
      print('\n老黑:ok啊 赢了好吧 你也是没有实力啊……')
      c += 1

    elif(pl == "剪刀" and com == "石头"):
      print("老黑得分！")
      print("\n老黑：你有实力吗 你就在这bb")
      c += 1
    elif(pl == "scissor" and com == "paper"):
      print("玩家 " + n + " 得分！")
      print("\n老黑：牛皮 有本事玩到最后看结果啊！ ")  
      p += 1

print("\n\n最终得分 " + n + ": " + str(p) + " | 老黑: " + str(c))
if p == c:
    print("平局!!")
    print("\n老黑：卧槽居然没有分出胜负 敢不敢再来一把")
elif p > c:
    print("你赢了！")
    print("\n老黑：我c 这把不算 再来一把啊！")
else:
    print("老黑赢！！")
    print("\n老黑：我靠 赢你那不是有手就行吗？！")

