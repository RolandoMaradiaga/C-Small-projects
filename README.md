# C-Small-projects
C++ Guide 
#include <iostream>
#include <vector>
using namespace std;


int main()
{ 
    bool menu {true};
    char selection {};
    vector<int> vector_size{};
    while (menu){
        
    cout << endl <<"P - Print Numbers \nA - Add a Number.\nM - Display mean of the numbers.\nS - Display the Smallest number.\nL - Display the Largest Number.\nQ - Quit" << endl;
    cout << "Choose an option: ";
    cin >> selection;
    
    switch (selection) {
    
        
    case 'p':
    case 'P': {
        if ( vector_size.size() == 0)
         cout << "[] - The List is empty!" << endl;
      else 
         cout << "[ ";
         for (int i = 0; i < vector_size.size(); i++)
             cout << vector_size[i] << " ";
         cout << " ]";
       
       break; }
    case 'a':
    case 'A':{
        
        cout << "Please enter a number: ";
        int number;
        cin >> number;
        vector_size.push_back(number);
        cout << endl << number << " added!" << endl;
    break;
        }
    case 'm':
    case 'M':{
        
        double sum_of_vector {};
        double average {};
        
            if(vector_size.size() == 0)
                cout << "Unable to calculate!" << endl;
            else 
                for (auto sum: vector_size)
                sum_of_vector += sum;
                
                cout << "The average is: " << static_cast<double>(sum_of_vector) / vector_size.size() << endl;
        
       break; 
    }
        // 3 5 2
    case 's':
    case 'S':{
    
            if (vector_size.size() = 0){ 
                cout << "Unable!!" << endl;
               
             else { 
                 int min_num = vector_size[0];
                 for (auto nums: vector_size)
                    if (nums < min_num)
                min_num = vector_size[i];
            
            }
        cout << min_num;
        break;
        
    }
    case 'l':
    case 'L': {
        // 3 4 5 2
        int max_num = vector_size[0];
        
        for (int i = 1; i < vector_size.size(); i++){
            if (vector_size[i] > max_num) 
                max_num = vector_size[i];
             else 
                max_num = vector_size[0];
        
        }
        cout << max_num;   
break; 
    }
    
    case 'q':
    case 'Q': {
        menu = false;
        break;
    }
    default: cout << "Enter a valid option." << endl;
    
}
}
}
