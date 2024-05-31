public class Character {
    protected String name;
    protected int health;
    protected int mana;
    protected int level;

    public Character(String name, int health, int mana, int level) {
        this.name = name;
        this.health = health;
        this.mana = mana;
        this.level = level;
    }

    public void attack(Character target) {
        System.out.println(this.name + " attacks " + target.name + "!");
    }

    public void defend() {
        System.out.println(this.name + " defends!");
    }

    public void castSpell(Character target) {
        System.out.println(this.name + " casts a spell on " + target.name + "!");
    }

    public void levelUp() {
        this.level++;
        System.out.println(this.name + " leveled up to " + this.level + "!");
    }
}

public class RPGGame {
    public static void main(String[] args) {
        Warrior warrior = new Warrior("Patrick", 40, 70, 2, 65, 15);
        Mage mage = new Mage("SpongeBob", 100, 70, 1, 15, 50);
        Rogue rogue = new Rogue("Squidward", 50, 90, 3, 75, 30);

        warrior.attack(mage);
        mage.castFireball(warrior);
        rogue.backstab(warrior);

        warrior.levelUp();
        mage.levelUp();
        rogue.levelUp();
    }
}

class Mage extends Character {
    private int intelligence;
    private int spellPower;

    public Mage(String name, int health, int mana, int level, int intelligence, int spellPower) {
        super(name, health, mana, level);
        this.intelligence = intelligence;
        this.spellPower = spellPower;
    }

    public void castFireball(Character target) {
        System.out.println(this.name + " gets a gun and shoots " + target.name + "!");
    }
}

class Rogue extends Character {
    private int agility;
    private int dexterity;

    public Rogue(String name, int health, int mana, int level, int agility, int dexterity) {
        super(name, health, mana, level);
        this.agility = agility;
        this.dexterity = dexterity;
    }

    public void backstab(Character target) {
        System.out.println(this.name + " does a sidekick to " + target.name + "!");
    }
}
public class RPGGame {
    public static void main(String[] args) {
        Warrior warrior = new Warrior("Patrick", 40, 70, 2, 65, 15);
        Mage mage = new Mage("SpongeBob", 100, 70, 1, 15, 50);
        Rogue rogue = new Rogue("Squidward", 50, 90, 3, 75, 30);

        warrior.attack(mage);
        mage.castFireball(warrior);
        rogue.backstab(warrior);

        warrior.levelUp();
        mage.levelUp();
        rogue.levelUp();
    }
}
