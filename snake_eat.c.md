    #include<stdio.h>
    #include<stdlib.h>
    #include <ctime>

    #define SNAKE_MAX_LENGTH 20
    #define SNAKE_HEAD 'H'
    #define SNAKE_BODY 'X'
    #define BLACK_CELL ' '
    #define SNAKE_FOOD '$'
    #define WALL_CELL '*'

    void snakemove(int a,int b);//move (up down left right)  
    void putmoney(void);//put a food randomly on a blank cell
    void output(void);//put out
    int gameover(void);//end the game 

    char map[12][13]={"************",
				  "*XXXXH     *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "*          *",
				  "************"};

    int len=5;// 蛇的长度 

    int y[20]={1,2,3,4,5};	//蛇的坐标	
    int x[20]={1,1,1,1,1};		

    int main() {
	char single;
	
	putmoney();
	
	output();
	
	while(gameover()==0) {
		
		scanf("%c",&single);
		 
		switch(single) {
			case 'A':
				snakemove(0,-1);
				break;
			case 'D':
				snakemove(0,1);
				break;
			case 'W':
				snakemove(-1,0);
				break;
			case 'S':
				snakemove(1,0);
				break;
		}
		
		output();
		
		if(gameover()) {
			
			printf("GAME OVER!!!\n");
			
			return 0;
		}
		
	}
	
	return 0;
	
    }

    void snakemove(int a,int b){
	
     int i;
   
     for(i=0;i<len;i++){
   	   map[x[i]][y[i]]=' ';//把原先的HHHHX变为空 
    }
    if(map[x[len-1]+a][y[len-1]+b]=='$'){
   	 len++;
   	 
	 x[len-1]=x[len-2]+a; 
	 y[len-1]=y[len-2]+b;
	 map[x[len-1]][y[len-1]]=' ';
	 
	 putmoney();
    }
    else{
     for(i=0;i<len-1;i++){
   	   x[i]=x[i+1];   //除头部以外 每一位的位置是上一位的位置 
	   y[i]=y[i+1]; 
     }
       x[len-1]+=a;//头部移动（上，下，左，右） 
	   y[len-1]+=b;
	}
    }
    void output(void){
     int i;
  
     for(i=0;i<len;i++){
   	   map[x[i]][y[i]]='X';
     }
     
     map[x[len-1]][y[len-1]]='H';//重新赋予HHHHX 
     
	 system("cls"); //from help from others(清屏操作)
     
	 for(i=0;i<12;i++){
  	   printf("%s\n",map[i]);//输出 
     } 
    }  

    int gameover(void){
	int i;
	
	for(i=0;i<len-1;i++){
	  if(x[len-1]==x[i]&&y[len-1]==x[i])//蛇撞到自己，必有坐标重复 
	  	  return 1;
    }
    
	if(x[len-1]<=10&&x[len-1]>=1&&y[len-1]<=10&&y[len-1]>=1)//蛇的坐标未过界 
	  return 0;
	else
	  return 1;
	
    }  
    void putmoney(void){
	int money_x,money_y;
	
	srand((unsigned)time(0));
	
	money_x=rand()%10+1;
	money_y=rand()%10+1;
	
	while(map[money_x][money_y]!=' '){
	 money_x=rand()%10+1;
	 money_y=rand()%10+1;
	  
    }
    map[money_x][money_y]='$';
}