#include <<iostream>>

#include <<string>>

#include <<sstream>>

#include <<vector>>

using namespace std;

void split_list(vector<int> input_array, int middle_value) {

    int count = 0;
    
    vector<int> less_list = {};
    
    vector<int> more_list = {}; 
    
    vector<int> equal_list = {}; 
    
    for (int i : input_array) {
    
        count++;
        
    }
    
    for (int index = 0; index < count; index++) {
    
        if (input_array[index] < middle_value) {
        
            less_list.push_back(input_array[index]);
            
        } else if (input_array[index] > middle_value) {
        
            more_list.push_back(input_array[index]);
            
        } else {
        
            equal_list.push_back(input_array[index]);
            
        }
        
    }
    
    cout << "Less than middle value list: ";
    
    for (int x : less_list) {
    
        (x != less_list.back()) ? (cout << x << ", "): (cout << x);
        
    }
    
    cout << endl;
    
    cout << "Equal to middle value list: ";
    
    for (int x : equal_list) {
    
        (x != equal_list.back()) ? (cout << x << ", "): (cout << x);
        
    }
    
    cout << endl;
    
    cout << "More than middle value list: ";
    
    for (int x : more_list) {
    
        (x != more_list.back()) ? (cout << x << ", "): (cout << x);
        
    }
    
    cout << endl;
    
}

int main() {

    vector<int> input = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    
    split_list(input, 3);
    
    return 0;
    
}
