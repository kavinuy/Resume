import java.util.*;
import java.io.*;
import java.applet.Applet;
import java.awt.*;

public class Resume {

   
    public static void main(String[] args) {
        String Name,College,Email,Address;
        int ConNum;
        Scanner Input = new Scanner(System.in);
        ArrayList<String> ResumeInfo = new ArrayList<String>();
       
        System.out.println("Please Input your Name");
        Name = Input.nextLine();
        ResumeInfo.add(Name);
       
        System.out.println("Please Input your Address");
        Address = Input.nextLine();
        ResumeInfo.add(Address);
       
        System.out.println("Please Input the Name of the College You've attended");
        College = Input.nextLine();
        ResumeInfo.add(College);
       
        System.out.println("Please Input your Email Address");
        Email = Input.nextLine();
        ResumeInfo.add(Email);
       
        System.out.println("Please Input your contact number");
        Email = Input.nextLine();
        ResumeInfo.add(Email);
       
       
       
       
        try{
            Object objArr[] =ResumeInfo.toArray();
            FileWriter fstream = new FileWriter("out.html");
            BufferedWriter out = new BufferedWriter(fstream);
            out.write(("Name: " + objArr[0]));
            out.write("Address: " + objArr[1]);
            out.write("College Attended: " + objArr[2]);
            out.write("Email Address: " + objArr[3]);
            out.write("Contact Number: " + objArr[4]);
            out.write("<img src= \"https://fbcdn-profile-a.akamaihd.net/hprofile-ak-snc4/186364_1328238710_534423856_n.jpg\" height =\"200\" width=\"200\">");
            out.close();
            }
            catch (Exception e)
            {
            System.out.println("ERROR!!");
            }

    }

}