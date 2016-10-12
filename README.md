# GetAge
To know your present age along with the name using constructor


code:

using System;

public class Person
{
	public Person(string firstName, string lastName)
	{
		FirstName = firstName;
		LastName = lastName;
	}
	
	public string FirstName { get; set; }
	
	public string LastName { get; set; }
	
	public DateTime DateOfBirth { get; set; }
	
	public string GetFullName()
	{
		return FirstName + " " + LastName;
	}
	public int GetAge()
	{
		return DateTime.Now.Year - DateOfBirth.Year;
	}
}

public class Program
{
	public static void Main()
	{
Person pr=new Person(Console.ReadLine(),Console.ReadLine());
		pr.DateOfBirth=Convert.ToDateTime(Console.ReadLine());
		int age;
		age=pr.GetAge();
		Console.WriteLine(age);
	}
}
