//This is code to make a simple currency converter
#include<iostream>
using namespace std;
//1 Indian Rupee equals 0.011 Euro
// 1 Euro equals 90.87 Indian Rupee
// 1 Pound sterling equals 101.68 Indian Rupee
//Funtions declaration
int INR_usd(int INR);
int USD_inr(int USD);
int EUR_inr(int EUR);
int INR_eur(int INR);
int POUND_inr(int POUND);
int INR_pound(int INR);
void  ask (int a);
//main funtion 
int main(){
    int a;
    ask(a);
    for(int i = 1;i<10000,i++;){
        string reuse;
        cout<<"\n\n Do you want to convert more\n Yes/No "<<endl;
        cin>>reuse;
        
        if(reuse =="Yes"){
            ask(a);
        }
        else{
            break;
        }
    }
    return 0;
}
//ask funtion
void  ask(int  a){
    cout<<"Which currency do you want to convert :\n 1.INR TO USD\n 2.USD TO INR\n 3.EUR TO INR\n 4.INR TO EUR\n 5.POUND TO INR\n 6.INR TO POUND\n Write your answer in number"<<endl;
    cin>>a;
    if (a ==1){
        int INR;    
        cout<<"Enter rupees"<<endl;
        cin>>INR;
        INR_usd(INR);
    }
    else if (a ==2)
    {
        int USD;
        cout<<"Enter Doller"<<endl;
        cin>>USD;
        USD_inr(USD);
    }
    else if (a==3){
        int EUR;
        cout<<"Enter Euro"<<endl;
        cin>>EUR;
        EUR_inr(EUR);
    }
    else if(a ==4){
        int INR;
        cout<<"Enter Indian rupee"<<endl;
        cin>>INR;
        INR_eur(INR);
    }
    else if (a==5){
        int POUND;
        cout<<"Enter Pound"<<endl;
        cin>>POUND;
        POUND_inr(POUND);
    }
    else if (a ==6){
        int INR ;
        cout<<"Enter Indian rupee"<<endl;
        cin>>INR;
        INR_pound(INR);
    }    

}
//INR_usd funtion
int INR_usd(int INR){
    
    float INR_USD  = INR/81.55;
    cout<<"\n\n"<<INR<<" Rupees is equal to "<<INR_USD<<" United States Dollar"<<endl;
    return 0;
}
//USD_inr funtion
int USD_inr(int USD){
    float USD_INR = (USD*81.55);
    cout<<"\n\n"<<USD<<" United States Dollar is equal to "<<fixed<<USD_INR<<" Indian rupees"<<endl;
    return 0;
}
// EUR_inr function
int EUR_inr(int EUR){
    float EUR_INR  = (EUR*90.87);
    cout<<"\n\n"<<EUR<<" European currency is equal to "<<fixed<<EUR_INR<<" Indian rupees"<<endl;
    return 0;
}
//INR_eur function
int INR_eur(int INR){
    float INR_EUR = (INR/90.87);
    cout<<"\n\n"<<INR<<" Indian rupees is equal to "<<INR_EUR<<" Euro"<<endl;
    return 0;
}
//POUND_inr function
int POUND_inr(int POUND){
    float POUND_INR = POUND*101.68;
    cout<<"\n\n"<<POUND<<" Pound is equal to "<<fixed<<POUND_INR<<" Indian rupees"<<endl;
    return 0 ;
}
//INR_pound function
int INR_pound(int INR){
    float INR_pound = INR/101.68;
    cout<<"\n\n"<<INR<<" Indian rupees is equal to "<<float(INR_pound)<<" Pounds"<<endl;
    return  0;
}
