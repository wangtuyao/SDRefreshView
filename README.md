# SDRefreshView
简单易用的上拉和下拉刷新（多版本细节适配）

1.导入主头文件

    #import "SDRefresh.h"

2.创建并设置 （只需3步）
    
    SDRefreshHeaderView *refreshHeader = [SDRefreshHeaderView refreshView];
    
    [refreshHeader addToScrollView:目标tableview]; // 加入到目标tableview
    
    [refreshHeader addTarget: refreshAction:加载内容的方法] 或者 refreshHeader.beginRefreshingOperation = ^{} 任选其中一种即可
    
----------------------------------------------------------------------------------------------------------------
  PS： 
  1. 如果需要一进入就自动加载一次数据，请调用[refreshHeader beginRefreshing];
  2. 默认是在navigationController环境下，如果不是在此环境下，请设置 refreshHeader.isEffectedByNavigationController = NO;
   
   
    