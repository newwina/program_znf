# program_znf
关于云平台技术的实验仓库
#include<bits/stdc++.h>
using namespace std;
const int N = 10;
int path[N];
bool st[N];
int n;
void dfs(int u)
{
    if( u == n )
    {
        for(int i = 0 ; i < n ; i++) printf("%d " , path[i] );
        puts("");
        return;
    }
    else
    {
        for(int i = 1; i <= n ; i++)
        {
            if( !st[i] )
            {
                path[u] = i;
                st[i] = true;
                dfs( u + 1 );
                st[i] = false; 
            }
        }
    }

}

int main()
{
    cin >> n;
    dfs(0);
    return 0;
}
