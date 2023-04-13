#include <iostream>
#include <string>
#include <vector>

using namespace std;

class Contact {
public:
    string name;
    string phone;
    string email;
    
    Contact() {}
    
    Contact(string n, string p, string e) {
        name = n;
        phone = p;
        email = e;
    }
};

class AddressBook {
public:
    vector<Contact> contacts;
    
    void addingcontact(Contact c) {
        contacts.push_back(c);
    }
    
    void deletecontact(int index) {
        contacts.erase(contacts.begin() + index);
    }
    
    void showcontacts() {
        for (int i = 0; i < contacts.size(); i++) {
            cout << "Contact " << i+1 << ":" << endl;
            cout << "Name: " << contacts[i].name << endl;
            cout << "Phone: " << contacts[i].phone << endl;
            cout << "Email: " << contacts[i].email << endl;
        }
    }
};

int main() {
    AddressBook ab1;
    int choice;
    
    do {
        cout << "Choose an option:" << endl;
        cout << "1. Add a contact" << endl;
        cout << "2. Remove a contact" << endl;
        cout << "3. Print the contacts" << endl;
        cout << "4. Quit the Program" << endl;
        cin >> choice;
        
        switch(choice) {
            case 1: {
                string name, phone, email;
                cout << "Enter the name: ";
                cin >> name;
                cout << "Enter the phone number: ";
                cin >> phone;
                cout << "Enter the email id: ";
                cin >> email;
                Contact c(name, phone, email);
                ab1.addingcontact(c);
                break;
            }
            case 2: {
                int index;
                cout << "Enter index of contact to remove: ";
                cin >> index;
                ab1.deletecontact(index-1);
                break;
            }
            case 3: {
                ab1.showcontacts();
                break;
            }
            case 4: {
                cout << "See you again!" << endl;
                break;
            }
            default: {
                cout << "Invalid choice." << endl;
                break;
            }
        }
    } while (choice != 4);
    
    return 0;
}
