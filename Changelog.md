# **Changelog**

## Version 0.13 beta
1. You will now only execute once every time you change a position.
2. Set each transaction step as a function.
3. Now, You can get the amount of equity change each time the strategy is executed. *0.13.1*

## Version 0.12 beta

1. Now, You can get account equity from every time the strategy is executed.
2. ~~for-loop the transaction twice to prevent server port error.~~ *v0.13 delete*
3. add KD_Strategy

### 代辦事項
#### 功能項目
1.
```
def long_a_position and short_a_position and close_position
```

2.
```
def set_current_position
```

3.
```
current_position=-1,0,1,2(-1:short,0:close,1:long,2:stop_profit or loss)
```

4.
```
if signal[0] > 0 and (current_position == 1 or current_postion == 2):
     None   
else:
     long_a_position
     current_position = 1
     
if signal[0] > 0 and (current_position == 1 or current_postion == 2):
     None   
else:
     short_a_posision
     current_position = 1
```
5.
```
if (cross_signal[0] == 1) or (cross_signal[0] == -1):
    print('行情反轉重設目前持倉模式')
    current_position = 0
```

6.
```
dic={0.05:0.03,
    0.08:0.05,
    0.12:0.08
    0.15:0.12
    0.18:0.15}
equity_percent_change = current_equity/initial_equity




```




1. plot K線與EMA疊圖 (用以Line推播通知)
2. 將交易對設置為變數
3. 試著計算每次作多與做空交錯時總損益 (用以Line推播通知、製成Dataframe匯出成csv) ----- *v0.14 1/2 finish*
> 可以設個temp在每次執行作多做空策略時紀錄下當下錢包總金額
4. 實作逐倉交易對策略執行 (須完成2.)
5. 實作策略的停利停損
6. 優先將signal修正回1,0,-1判斷，在執行策略時以while執行每一step確保幣安伺服交易成功 ----- *v0.13 finish*
7. 提供策略選項


#### 策略項目
1. 試著找尋是否有相關指標以判斷當前行勢是否處於區間震盪(布林帶寬)
2. 

##### 提問
* 

```
if 'Cacul_profit' in globals():
    profit_loss = -Cacul_profit
```