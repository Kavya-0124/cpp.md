# cpp.md

<details>
  <summary>code</summary>
  
  ~~~~
  
  #include<iostream>
#include<string>
using namespace std;
class atm{
    private:
        long int account_number;
        string name;
        int pin;
        double balance;
        string mobile_no;

    public:
    void setdata(long int accoun_number_a, string name_a, int_pin_a, double_balance_a, string mobile_no_a ){
        account_number=account_number_a;
        name=name_a;
        pin=pin_a;
        balance=balance_a;
        mobile_no=mobile_no_a;
    } 
    long int getaccount_number(){
        return account_number;
    }

    string getname(){
        return name;
    }

    int getpin(){
        return pin;
    }

    double getbalance(){
        return balance;

    }

    string getmobile_number(){
        return mobile_number;
    }

    void setMobile(string mob_prev, string mob_new){
        if(mob_prev=mobile_number){
            mobile_number=mob_new;
            cout<<endl<<"Successfully updated";
            _getch();
        }

        else{
            cout<<endl<<"Invalid Input or Insufficient balance";
            _getch();
        }
    }
};

int main()
{
    int choice=0; enterpin;
    long int enteraccount_number;

    system("cls");

    atm u1;
    u1.setData(12345, "Tim", 1111, 45000.00, 7260816653);
    do
    {
        system("cls");

        cout<<endl<<"***Welcome to ATM"<<endl;
        cout<<endl<<"Enter Your Account number";
        cin>>enteraccount_number;

        cout<<endl<<"Enter pin";
        cin>>enterpin;

        if((enteraccount_number==u1.getaccount_number()) && (enterpin==u1.getpin()))
        {    
             do
             {
              int amount=0;
              string mobile_number, new mobile_number;
              system("cls");

              cout<<endl<<"***Welcome***";
              cout<<endl<<"Select options";
              cout<<endl<<"1 Check balance";
              cout<<endl<<"2 Cash withdraw";
              cout<<endl<<"3 Show user details";
              cout<<endl<<"4 Update Mobile number";
              cout<<endl<<"5 Exit";
              cin>>choice;

               switch(choice)
               {
                 case 1:
                 cout<<endl<<"Your balance is:"<<u1.getbalance();
                 _getch();
                 break;

                 case 2:
                 cout<<endl<<"Enter the amount";
                 cin>>amount;
                 u1.cashwithdraw(amount);
                 break;

                 case 3:
                 cout<<endl<<"***User Details***";
                 cout<<endl<<"Account number"<<u1.getaccount_number;
                 cout<<endl<<"Name"<<u1.getname();
                 cout<<endl<<"Balance"<<u1.getbalance();
                 cout<<endl<<"Mobile Number"<<u1.getmobile_number();

                 _getch();
                 break;

                 case 4:
                 cout<<endl<<"Enter old mobile number";
                 cin>>mobile_number;

                 cout<<endl<<"Enter New mobile number";
                 cin>>newmobile_number;

                 u1.setmobile(oldmobile_number, newmobile_number);
                 break;

                 case 5:

                 exit(0);

                 default:
                 cout<<endl<<"Enter Valid info!!!";

                }   
            } while(1);
        }
        else
        {
            cout<<endl<<"User details are Invalid!!!";
          _getch();
        }
    }
    while(1);
    return 0;
}
  
  ~~~
  
  </details>
