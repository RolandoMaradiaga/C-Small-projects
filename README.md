#include <iostream>
#include <string>
using namespace std;

int main() {
    
    string alphabet {"abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"};
    string key  {"XZNLWEBGJHQDYVTKFUOMPCIASRxznlwebgjhqdyvtkfuompciasr"};
    string secrete_message {};
    
    cout << "Enter your secrete message: ";
    getline(cin, secrete_message);
    cout << "\n";
    
    string encrypted_message{};
    string original_message{};
    
    for (char c: secrete_message){
        size_t position = alphabet.find(c);
        if (position != string::npos){
            char new_c{key.at(position)};
            encrypted_message += new_c;
            
        } else {
            encrypted_message+= c;
        }
        
    
    }
    cout << encrypted_message << endl;
    
    for (char d: encrypted_message){
    size_t position = key.find(d);
    if (position != string::npos){
        char new_d {alphabet.at(position)};
    original_message += new_d;}
    else { 
    original_message += d;}
        
    }   
    
        cout <<"\n" << original_message << endl; 
        
    
    
    return 0;
}

