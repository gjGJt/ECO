  #include <iostream>
#include <string>  
using namespace std;

int main() {  
    int increase, decrease, derivative, incdec, locavg, originp, updp, cpione, cpitwo, exone, whyone, extwo, whytwo, ceepiiy;  
    string global;  
    cout << "Do you want to calculate the percent change, consumer price index, average rate?" << endl; 
    cin >> global;  

   if(global == "Percent Change") { 
        cout << "Enter the original price: " << endl;  
        cin >> originp;  
        cout << "Enter the updated price: " << endl;  
        cin >> updp;  

   if(originp > updp) {
            decrease = ((originp - updp) / (double)originp) * 100;  
            cout << "The inflation rate is " << decrease << " %" << endl;  
        } else if(updp > originp) {  
            increase = ((updp - originp) / (double)originp) * 100;  
            cout << "The increase rate is " << increase << " %" << endl;  
        }
    } else if(global == "Average") {  
        cout << "Enter one x value: " << endl;  
        cin >> exone;  
        cout << "Enter another x value: " << endl;  
        cin >> extwo;  
        cout << "Enter a y value: " << endl;  
        cin >> whyone;  
        cout << "Enter another y value: " << endl;  
        cin >> whytwo;  
        derivative = ((whytwo - whyone) / (extwo - exone)); 
        cout << "Your average is " << derivative << endl;  
    } else if(global == "CPI") {  
        cout << "Enter the new price index: " << endl;  
        cin >> cpione;  
        cout << "Enter the previous price index: " << endl;  
        cin >> cpitwo;  
        ceepiiy = (int)((cpione / (double)cpitwo) * 100);  
        cout << "The consumer price index rate is " << ceepiiy << endl; 
    }

   return 0;  
}

