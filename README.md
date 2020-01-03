echo "# ATM_Account_Project" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Zane-Torregrossa/ATM_Account_Project.git
git push -u origin master


import random 

class Account:
  # Constuct an Account object
  def __init__(self, id, balance = 0, annualInterestRate = 3.4):
    self.id = id
    self.balance = balance
    self.annualInterestRate = annualInterestRate
   
  def getId(self):
    return self.id
    
  def getBalance(self):
    return self.balance
  
  def getAnnuanlInterestRate(self):
    return self.annualInterestRate
     
  def getMonthlyInterestRate(self):
    return self.annualInterestRate / 12
    
  def withdraw(self, amount):
    self.balance -= amount
    
  def deposit(self, amount):
    self.balance += amount
    
  def getMonthlyInterest(self):
     return self.balance * self.getMonthlyInterestRate()
     
