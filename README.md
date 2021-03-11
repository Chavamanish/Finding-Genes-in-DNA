# Finding-Genes-in-DNA
developed an algorithm for finding multiple genes within a DNA string by locating the start and stop codons and converting it into a program  as well as tackling other string related problems.

public class part1 {
    public String findsimplegene(String dna)
    {
        String result="";
       int startpos= dna.indexOf("ATG");
       System.out.println(startpos);
       if(startpos==-1)
       {return "";
        }
        int endpos=dna.indexOf("TAA",startpos+3);
        System.out.println(endpos);
        if(endpos==-1)
        {return "";
        }
        result=dna.substring(startpos,endpos+3);
        
        if(((startpos+3)-endpos)%3==0)
        {
        return result;
        }
        else{
            return "";

    }
}
    public void testsimplegene()
    {
        String dna="ACATGTCGGCTTCATAAG";
        System.out.println("The DNA is:" +dna);
        String s=findsimplegene(dna);
        System.out.println("The Gene is:" +s);
        
        dna="ACATGTCGGCTTCTAAG";
        System.out.println("The DNA is:" +dna);
        s=findsimplegene(dna);
        System.out.println("The Gene is:" +s);
        
        dna="ACATATCGGCTTCATAAG";
        System.out.println("The DNA is:" +dna);
        s=findsimplegene(dna);
        System.out.println("The Gene is:" +s);
        
       



        

    }
    
}
