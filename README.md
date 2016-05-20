# Bank-account-class-copy-constructer
this program accepts a BankAccount object as an argument. It should assign to the balance field the value in the argument's balance field. As a result, the new object will be a copy of the argument object.


public class BankAccount
{
    private double balance;

    public BankAccount(double b)
    {
        balance = b;

    }

    public BankAccount(BankAccount obj)
    {
        balance = obj.balance;
    }



    public double getBalance()
    {
        return balance;
    }


}




public class BankAccountCopy
{
    public static void main(String[] args) {


        BankAccount account1 = new BankAccount(1000.0);

        BankAccount account2 = new BankAccount(account1);

        DecimalFormat dollar = new DecimalFormat("#,##0.00");


        System.out.println("Account #1 has a balance of $"
                            + dollar.format(account1.getBalance()));
        System.out.println("Account #2 has a balance of $"
                            + dollar.format(account2.getBalance()));


    }
}
