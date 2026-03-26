This bot copies the HLP vault positions and atttempts to track the current positions as well as all trades 
Adjusted to websocket for fills ( can adjust to polls as you wish ).

heres how the HLP vault works 
By splitting into two sub-accounts, each one can hold a clean long or short position independently. They don't need to close one side before opening the other — Child A just stays long, Child B stays short, and the vault collects the spread from both sides simultaneously.

HLP acts as the parent vault for other strategies such as A, B, and Liquidator, with total TVL represented by HLP including its child strategies. But this parent-child structure is a protocol-level privilege — it's specific to HLP and the other protocol vaults. 

If it were a single account, you'd have to net everything — closing a long to go short means realizing losses, paying fees, and missing the bid-ask spread in between. Two accounts let you market-make both sides of the book cleanly without those issues.

