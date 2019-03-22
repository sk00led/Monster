# Monster
public class Main {
    public static void main(String[] args) {
        
# Declare two Weapon variables, instantiate two Weapon objects (using the parameterized constructor), and assign one of these Weapon objects to each of the two Weapon       //variables. You may choose any name and any maxDamage values you wish.
    Weapon weapon1 = new Weapon("Thunderbolt", 5000);
    Weapon weapon2 = new Weapon("Atomic Fire Breath", 100000);    
    
# Declare two Monster variables, instantiate two Monster objects, and assign 
# one of these Monster objects to each of the two Monster variables. Pass the Weapon objects       
# created in the previous step to constructors for the Monsters when you instantiate them. 
# You may choose any name and health values that you wish.  
    Monster monster1 = new Monster("Pikachu", 100000, weapon1);
    Monster monster2 = new Monster("Godzilla", 1000000, weapon2);
    
# Construct a loop that will iterate until one (or both) of the Monsters 
# has a health value that is less than or equal to zero. Within this loop:
    while (monster1.getHealth() > 0 && monster2.getHealth() > 0) {
        int damageDone1 = 0;
        int damageDone2 = 0;
        
# Call the attack method of each Monster 
# (be sure to capture the int returned by the attack method)
        damageDone1 = monster1.attack(monster2);
        damageDone2 = monster2.attack(monster1);
        
# Display a message describing the attacks e.g. 
# "Batra attacks Mothra with laser beams doing 100 points of damage."
        System.out.println(monster1.getName() + " attacks " + monster2.getName() + " doing " + damageDone1 + " points of damage!");
        System.out.println(monster2.getName() + " attacks " + monster1.getName() + " doing " + damageDone2 + " points of damage!");
        System.out.println();
        
        System.out.println(monster1.getName() + " health is  " + monster1.getHealth());
        System.out.println(monster2.getName() + " health is  " + monster2.getHealth());
        
        System.out.println("--------------------------------------------");
    }
        
        System.out.print("The winner is ");
        if (monster1.getHealth() > 0)
            System.out.println(monster1.getName() + "!!!");
        else if (monster2.getHealth() > 0)
            System.out.println(monster2.getName() + "!!!");
        else 
            System.out.println(" no one!!!");
    }

    
# Display the current health value of each Monster
    
# After the loop (described above) exits, display a message indicating which (if either) 
# Monster is still alive, and has therefore won the battle.
}
