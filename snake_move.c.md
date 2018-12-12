    #include<stdio.h>
    #include<stdlib.h>

    #define SNAKE_MAX_LENGTH 20
    #define SNAKE_HEAD 'H'
    #define SNAKE_BODY 'X'
    #define BLACK_CELL ' '
    #define SNAKE_FOOD '$'
    #define WALL_CELL '*'

    void snakemove(int a,int b);//move (up down left right)  
    void putmoney(void);//put a food randomly on a blank cell
    void output(void);//outs when game over
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

    int snake_length=5;

    int y[20]={1,2,3,4,5};	//蛇的坐标	
    int x[20]={1,1,1,1,1};		

    int main() {
	char single;
	
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
   
     for(i=0;i<5;i++){
   	   map[x[i]][y[i]]=' ';//把原先的HHHHX变为空 
    }
   
    for(i=0;i<4;i++){
   	  x[i]=x[i+1];   //除头部以外 每一位的位置是上一位的位置 
	  y[i]=y[i+1]; 
     }
   
	  x[4]+=a;//头部移动（上，下，左，右） 
	  y[4]+=b;
    }
    void output(void){
     int i;
  
     for(i=0;i<4;i++){
   	   map[x[i]][y[i]]='X';
     }
     
     map[x[4]][y[4]]='H';//重新赋予HHHHX 
     
	 system("cls"); //from help from others(清屏操作)
     
	 for(i=0;i<12;i++){
  	   printf("%s\n",map[i]);//输出 
     } 
    }  
    int gameover(void){
	int i;
	
	for(i=0;i<4;i++){
	  if(x[4]==x[i]&&y[4]==x[i])//蛇撞到自己，必有坐标重复 
	  	  return 1;
    }
    
	if(x[4]<=10&&x[4]>=1&&y[4]<=10&&y[4]>=1)//蛇的坐标未过界 
	  return 0;
	else
	  return 1;
	
    }
 