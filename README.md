# Corporate-Sales-in-c-



#include <iostream>
#include<string>
// #include "windows.h"

using namespace std;



class DivSales

{
    
private:
    
    static int Year_Sales;
    int Qtrsale[4];
    
public:
    
    void AddSales (int sale1, int sale2, int sale3, int sale4)
    
    {
        Qtrsale[0] = sale1;
        Qtrsale[1] = sale2;
        Qtrsale[2] = sale3;
        Qtrsale[3] = sale4;
        
        Year_Sales = Year_Sales + sale1 + sale2 + sale3 + sale4;
    }
    
    int Sales(int n)
    
    {
        int value = Qtrsale[n];
        return value;
    }
    
    int getvalue()
    {
        return Year_Sales;
    }
    
};



int DivSales::Year_Sales;



int main()

{
 
    const int DS = 6;
    DivSales DivisionSale[DS];
    int quarter, division;
   
    for (division = 0; division < 6; division++)
        
    {
        
       
        int Qrt1, Qrt2, Qrt3, Qrt4;
        
        int Q;
        
        cout<<endl;
        cout << "Enter The Sales for Division #" << division + 1 << endl;
        cout<<endl;
        cout << "Enter the Quarter#1 Sale: ";
        cin >> Qrt1;
        Q = Qrt1;
        
        while(Qrt1<0)
        {
            cout<<"Please Enter Numbers greater than zero:"<<endl;
            cin>>Qrt1;
        }
        
        cout << "Enter the Quarter#2 Sale: ";
        cin >> Qrt2;
        Q = Qrt2;
        
        while(Qrt2<0)
        {
            cout<<"Please Enter Numbers greater than zero:"<<endl;
            cin>>Qrt2;
        }
        
        cout << "Enter the Quarter#3 Sale: ";
        cin >> Qrt3;
        Q = Qrt3;
        
        while(Qrt3<0)
        {
            cout<<"Please Enter Numbers greater than zero:"<<endl;
            cin>>Qrt3;
        }
        
        cout << "Enter the Quarter#4 Sale: ";
        cin >> Qrt4;
        Q = Qrt4;
       
        while(Qrt4<0)
        {
            cout<<"Please Enter Numbers greater than zero:"<<endl;
            cin>>Qrt4;
        }
        
       
        DivisionSale[division].AddSales(Qrt1,Qrt2,Qrt3,Qrt4);
        
    }
    
    cout << "\n--------------------------------------------\n";
    cout << "\t\t" << "\t\tQ1" << "\t" << "\tQ2" << "\t" << "\tQ3" << "\t" << "\tQ4" << endl;
    

    for (division = 0; division < 6; division++)
        
    {
        
        cout << "Division :" << division + 1;
        for (quarter = 0; quarter < 4; quarter++)
            
        {
            
           
            cout << "\t\t$" << DivisionSale[division].Sales(quarter);
            
        }
        
        cout << endl;
        
    }
    
    cout << "--------------------------------------------\n";
    cout << "\nTotal corporate sales for the year is: "<< "$" << DivisionSale[0].getvalue() << endl;
    
    cout<<endl;
    
    return 0;
    
}
