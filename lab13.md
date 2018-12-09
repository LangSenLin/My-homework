# OK,let's go!
# 任务一   &&   任务二  

###  sneak——move & snake——eat
![](http://m.qpic.cn/psb?/V12RJg2C0qahST/aHWDf1yiEnZDjDc6EP8QcKsSqeY5hMGp7U9XSCgqZ5w!/b/dEcBAAAAAAAA&bo=SwJBAgAAAAADByg!&rf=viewer_4)    
```
输出字符矩阵
	WHILE not 游戏结束 DO
		ch＝等待输入
		CASE ch DO
		‘A’:左前进一步，break 
		‘D’:右前进一步，break    
		‘W’:上前进一步，break    
		‘S’:下前进一步，break    
		END CASE
		输出字符矩阵
	END WHILE
	输出 Game Over!!!

while(life!=1) { 
    timeover=1; 
    start=clock(); 
    while((timeover=(clock()-start<=hard*100))&&!kbhit());    
    if(timeover) 
    { 
          direcation=getch(); 
    } 
  
    switch(direcation) 
    { 
        case 'w':turn_up();break; 
        case 's':turn_down();break; 
        case 'a':turn_left();break; 
        case 'd':turn_right();break; 
    } 
  } 
  return 0; 
} 

void turn_up()    /*向上移动*/
{ 
   system("cls"); 
   int i; 
   if ( (snakex[0]==1) || (map[snakex[0]-1][snakey[0]]==003) ) gameover(); else { 
   if (map[snakex[0]-1][snakey[0]]=='$') 
   { 
      put_money( snakey[0], snakex[0]-1 ); 
      lenght++; 
      map[snakex[lenght-1]][snakey[lenght-1]]=003; 
   } 
   for(i=lenght; i>0; i--) 
   { 
     snakex[i]=snakex[i-1]; 
     snakey[i]=snakey[i-1]; 
   } 
   map[snakex[lenght]][snakey[lenght]]=' '; 
   snakex[0]--; 
   for(i=lenght-1; i>0; i--) map[snakex[i]][snakey[i]]=003; 
   map[snakex[0]][snakey[0]]=002; 
   output(); 
   } 
   return; 
} 
  
  
void turn_down()     /*向下*/
{ 
   system("cls"); 
   int i; 
   if ( (snakex[0]==10) || (map[snakex[0]+1][snakey[0]]==003) ) gameover();else { 
   if (map[snakex[0]+1][snakey[0]]=='$') 
   { 
      put_money(snakey[0],snakex[0]+1); 
      lenght++; 
      map[snakex[lenght-1]][snakey[lenght-1]]=003; 
   } 
   for(i=lenght; i>0; i--) 
   { 
     snakex[i]=snakex[i-1]; 
     snakey[i]=snakey[i-1]; 
   } 
   snakex[0]++; 
   map[snakex[lenght]][snakey[lenght]]=' '; 
   for(i=lenght-1; i>0; i--) map[snakex[i]][snakey[i]]=003; 
   map[snakex[0]][snakey[0]]=002; 
   output(); 
   } 
   return; 
} 
  
  
void turn_left()   /*向左*/
{ 
   system("cls"); 
   int i; 
   if ( (snakey[0]==1) || (map[snakex[0]][snakey[0]-1]==003) ) gameover();else { 
   if (map[snakex[0]][snakey[0]-1]=='$') 
   { 
      put_money(snakey[0]-1,snakex[0]); 
      lenght++; 
      map[snakex[lenght-1]][snakey[lenght-1]]=003; 
   } 
   for(i=lenght; i>0; i--) 
   { 
     snakex[i]=snakex[i-1]; 
     snakey[i]=snakey[i-1]; 
   } 
   map[snakex[lenght]][snakey[lenght]]=' '; 
   snakey[0]--; 
   for(i=lenght-1; i>0; i--) map[snakex[i]][snakey[i]]=003; 
   map[snakex[0]][snakey[0]]=002; 
   output(); 
   } 
   return; 
} 
  
  
void turn_right()    /*向右*/
{ 
   system("cls"); 
   int i; 
   if ( (snakey[0]==21) || (map[snakex[0]][snakey[0]+1]==003) ) gameover();else { 
   if (map[snakex[0]][snakey[0]+1]=='$') 
   { 
      put_money(snakey[0]+1,snakex[0]); 
      lenght++; 
      map[snakex[lenght-1]][snakey[lenght-1]]=003; 
   } 
   for(i=lenght; i>0; i--) 
   { 
     snakex[i]=snakex[i-1]; 
     snakey[i]=snakey[i-1]; 
   } 
   map[snakex[lenght]][snakey[lenght]]=' '; 
   snakey[0]++; 
   for(i=lenght-1; i>0; i--) map[snakex[i]][snakey[i]]=003; 
   map[snakex[0]][snakey[0]]=002; 
   output(); 
   } 
   return; 
} 
```


尽力了