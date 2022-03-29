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