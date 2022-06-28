```c++
#include <string>
#include <vector>
#include <algorithm>

using namespace std;

vector<int> solution(vector<int> array, vector<vector<int>> commands) {
    vector<int> answer(commands.size(),0);
    
    vector<int>::iterator it;
    for(int i=0; i<commands.size(); i++)
    {
        int k=0;
        vector<int> cut_array;
        for(int j=commands[i][0]; j<=commands[i][1]; j++)
        {
            if(j==0)
            {
                cut_array.push_back(array[j]);
            }
            else
            {
                cut_array.push_back(array[j-1]);
            }
        }
        sort(cut_array.begin(),cut_array.end());
        answer[i] = cut_array[commands[i][2]-1];
        
    }
    return answer;
}
```