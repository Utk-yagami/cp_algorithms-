#pragma GCC optimize("O3")

#include <bits/stdc++.h>
using namespace std;

// Macros and constants
#define pb                push_back
#define rep(i,a,b)        for(ll i=a;i<b;i++)
#define rev(i,a,b)        for(ll i=a;i>=b;--i)
#define fastio()          ios_base::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL)
#define mod               1000000007
#define MOD1              998244353
#define INF               1e18
#define inf               1000000000
#define ppb               pop_back
#define ff                first
#define ss                second
#define PI                3.141592653589793238462
#define set_bits          __builtin_popcountll
#define all(x)            (x).begin(), (x).end()
#define scin(str)         getline(cin, str)


// Debugging Macros
#define debug(x) cerr << #x << " = " << x << endl
#define debug2(x, y) cerr << #x << " = " << x << ", " << #y << " = " << y << endl

// Input/Output initialization
void init_code() {
#ifndef ONLINE_JUDGE
freopen("inputf.txt", "r", stdin);
freopen("outputf.txt", "w", stdout);
#endif
}

// Aliases and Types
using ll = long long int ;
using vec = vector<ll>;
using pii=pair<ll,ll>;

// Global Constants
const int dx[4]{1, 0, -1, 0}, dy[4]{0, 1, 0, -1};  // for every grid problem!!
const int N=2e5+5;


void dfs(ll node, ll par, vector<ll> adj[],vector<vector<ll>>&dp){
  dp[node][0]=par;
   rep(i,1,30){
    dp[node][i]=dp[dp[node][i-1]][i-1];
    //dp[node][i]=dp[node2][i-1];
   }
   for(auto it:adj[node]){
    if(it!=par)dfs(it,node,adj,dp);
   }
}


  void light_0_yagami(){
       ll n;
       cin>>n;
       ll q;
       cin>>q;
       vector<ll> adj[n+1];
       rep(i,2,n+1){
          ll a;
          cin>>a;
          adj[a].pb(i);
          adj[i].pb(a);
       }
       vector<vector<ll>> dp(n+1,vector<ll>(30));
       
       dfs(1,0,adj,dp);
      // rep(i,1,n+1){
      //   rep(j,0,17)cout<<dp[i][j]<<" ";
      //   cout<<"\n";
      // }
       while(q--){
        ll node, k;
        cin>>node>>k;// print kth parent of node
        rev(i,29,0){
          if((k>>i)&1)node=dp[node][i];
        }
        if(node==0)node=-1;
        cout<<node<<"\n";
       }
    
    }


    

 
int main() {  
   init_code();
   fastio();
  ll t=1;
//cin>>t;
  while(t--)
{
  light_0_yagami();

   
}
} 
