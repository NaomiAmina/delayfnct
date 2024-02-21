#include "stm32f10x.h"
void TimeFunction(int Temps);

int main(void)
{ 	RCC->APB2ENR |=  0x00000014; 
		GPIOC->CRH = (GPIOC->CRH & 0xFF0FFFFF) | 0x00300000;
		GPIOA->CRL =  (GPIOA->CRL & 0xFFFFFFF0)| 0x00000008;
    while(1)
		{
   	if (GPIOA->IDR == 0x00000001)
			{
				  GPIOC->BSRR = 0x00002000;
			}
			TimeFunction(2);
			
		//	if (GPIOA->IDR == 0x00000002)
		//	{
			   GPIOC->BSRR = 0x20000000;			     
	  // 	}
			TimeFunction(2);	
		}
}

void TimeFunction(int Temps)
{ 
   int j,k;
      for (j=0;j<Temps;j++)
    {
        for (k=0;k<2882;k++)
        {
        }
    }
			
}
