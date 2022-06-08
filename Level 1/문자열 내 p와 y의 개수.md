```c++
#include <string>

using namespace std;

bool solution(string s)
{
    bool answer = true;
    int p_count=0;
    int y_count=0;
    
    for(int i=0; i<s.length(); i++)
    {
        if(s[i] == 112 || s[i] == 80)
        {
            p_count++;
        }
        else if(s[i] == 121 || s[i] == 89)
        {
            y_count++;
        }
    }
    
    if(p_count != y_count)
    {
        answer = false;
    }
    

    return answer;
}
```