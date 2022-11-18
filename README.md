# OOPExercise2
public class MainProgram{
	public static void main(String[] args){
		Animal animal;
		Bird bird = new Bird ("Tweety",5, "Alimukon");
		Chicken chicken = new Chicken ("Chingky", 2, "Bantam");
		
		animal=bird;
		System.out.println(animal.makesound()+ " "+ "My name is "+ animal.getName());
		
		animal=chicken;
		System.out.println(animal.makesound()+ " "+ "My name is "+ animal.getName());
		
	}
}

public abstract class Animal{
	
	protected String name;
	protected double weight;
	
	public Animal (String name, double weight){
		this.name = name;
		this.weight = weight;
	}
	public abstract String makesound();
	
	public String getName(){
		return name;
	}
   public  void setName (String name){
	   this.name = name;
   }
   public double getweight(){
	   return weight;
   }
   public void setweight (double weight){
	   this.weight=weight;
   }
   
}

public class Bird extends Animal{

	private String breed;
	
	public Bird (String name, double weight, String breed){
		super(name,weight);
		this.breed=breed;
	}

	@Override
	public String makesound(){
		// TODO: Implement this method
		return "Twit!Twit!";
	}
    public String getBreed(){
		return breed;
	}
	public void setBreed(String breed){
		this.breed=breed;
	}
	
}

public class Chicken extends Animal{
	private String farm;
	
	public Chicken (String Name, double weight, String farm){
		super(Name,weight);
		this.farm=farm;
	}

	@Override
	public String makesound()
	{
		// TODO: Implement this method
		return "Toktoga-ok!Toktoga-ok!";
	}
	public String getBreed(){
		return farm;
	}
	
	public void setFarm(String farm){
		this.farm=farm;
	}
}
