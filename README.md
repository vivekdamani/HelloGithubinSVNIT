
#include<bits/stdc++.h>
#include<stdio.h>
typedef long long ll;
#define pb push_back
#define mp make_pair
#define F first
#define S second
#define MOD 1000000007
using namespace std;
int main()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    ll n,t,m,i,j,k;
    cin>>t;
    while(t--)
    {
        //cin>>n;
        string s;
        cin>>s;
        stack<char>q;
        vector<char>v;
        n=s.size();
        m=0;
        k=0;
        if(n%2!=0)
        {
            cout<<"NO"<<endl;
        }
        else{
                j=0;
                
            for(i=n-1;i>=0;i--)
            {


                if(j==0)
                {
                    m=0;

                    j=-1;
                if(s[i]=='?')
                {
                    s[i]=')';
                    m++;
                }
                else if(s[i]=='(')
                {
                    k=-1;
                    break;
                }
                else{
                    m++;
                }
                }
                else{
                if(s[i]==')')
                {
                    m++;
                }
                else{
                    m--;
                    if(m==0)
                    {
                        j=0;
                    }

                }
                }
              //  cout<<m<<" "<<k<<endl;


            }
            //cout<<m<<" "<<k<<endl;
            if(k==-1 || m!=0)
            {
                cout<<"NO"<<endl;
            }
            else{
                    cout<<"YES"<<endl;
            }
        }




    }
return 0;
}

