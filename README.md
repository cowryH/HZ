# HZ
import java.awt.event.MouseEvent;

import java.util.Scanner;

public class shiyan4 {  

    @SuppressWarnings("resource")

public static void main(String args[])  

    {  

        Scanner in=new Scanner(System.in); //使用Scanner类定义对象  

        double numn[][] = new double [100][100]; 

        double goal[] = new double [100];

        double gan[] = new double [100];

        double max=0,min=100;

        double sum=0,G=0;

        System.out.println("请输入人数mump");  

        double nump=in.nextDouble(); //接收float型数据 

        System.out.println("请输入游戏次数mumg");  

        double numg=in.nextDouble(); //接收float型数

        for(int h=0;h<nump;h++){

         goal[h]=0;

         gan[h]=0;

        }

        for(int s=0;s<numg;s++)

        { 

             System.out.println("游戏开始");

       for(int k=0;k<nump;k++) { 

        System.out.println("由玩家输入估计的数值num值为整形");

        double num = in.nextDouble(); //接收float型数据

            numn[s][k]=num;    

            }

                                   

        for(int j=0;j<nump;j++)

        {

      sum+=numn[s][j];

          }

   

     G=(sum/nump)*0.618;//求G值  

      double dif=0;

      

     for(int qq=0;qq<nump;qq++){//求分数

     dif=Math.abs(numn[s][qq]-G);

     goal[qq]=dif;    

       }

        for(int f=0;f<nump;f++)

         {

            if(max<goal[f])

               max=goal[f];

            if(min>goal[f])

             min=goal[f];                

          }

         for(int th=0;th<nump;th++)

         {

          if(goal[th]==min)

          gan[th]=gan[th]+nump;

          if(goal[th]==max)

          gan[th]=gan[th]-2;

         }             

         

        for(int tt=0;tt<nump;tt++)

        {

         System.out.println(gan[tt]);

          }

        }        

}

}
