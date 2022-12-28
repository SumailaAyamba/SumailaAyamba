### Hi there 👋

<!--
**SumailaAyamba/SumailaAyamba** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on Python projects
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me:sumailaayamba14@gmail.com
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

##This program calculates the retirement benefit

CONTRIB_RATE=0.05
def main():
    grossPay=float(input("Please Enter the Gross pay:"))
    bonus=float(input("Pealse the amount of bonuses:"))
    showPayContrib(grossPay)
    showBonusContrib(bonus)
    
    
def showPayContrib(gross):
    contrib=gross*CONTRIB_RATE
    print("Contribution for the gross pay: $", format(contrib, ',.2f'), sep="")
    
def showBonusContrib(bonus):
    contrib=bonus*CONTRIB_RATE
    print("Contribution for bonuses: $", format(contrib, ',.2f'), sep="")
    
main()
    




