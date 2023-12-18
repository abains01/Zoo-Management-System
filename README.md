#include <iostream>
#include <vector>
#include <string>

class Animal {
public:
    std::string Name;
    int Age;
    std::string Diet;
    int Weight;

    Animal(const std::string& name, int age, const std::string& diet, int weight)
        : Name(name), Age(age), Diet(diet), Weight(weight) {}

    virtual ~Animal() {}

    virtual void DisplayInfo() const {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << std::endl;
    }
};

class Cheetah : public Animal {
public:
    Cheetah(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Cheetah" << std::endl;
    }
};

class Giraffe : public Animal {
public:
    Giraffe(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Giraffe" << std::endl;
    }
};

class Tiger : public Animal {
public:
    Tiger(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Tiger" << std::endl;
    }
};

class Elephant : public Animal {
public:
    Elephant(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Elephant" << std::endl;
    }
};

class Lion : public Animal {
public:
    Lion(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Lion" << std::endl;
    }
};

class Alligator : public Animal {
public:
    Alligator(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Alligator" << std::endl;
    }
};

class Peacock : public Animal {
public:
    Peacock(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Peacock" << std::endl;
    }
};

class Monkey : public Animal {
public:
    Monkey(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Monkey" << std::endl;
    }
};

class Eagle : public Animal {
public:
    Eagle(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Eagle" << std::endl;
    }
};

class Fish : public Animal {
public:
    Fish(const std::string& name, int age, const std::string& diet, int weight)
        : Animal(name, age, diet, weight) {}

    void DisplayInfo() const override {
        std::cout << "Name: " << Name << ", Age: " << Age
                 << ", Diet: " << Diet << ", Weight: " << Weight << ", Type: Fish" << std::endl;
    }
};

int main() {
    std::vector<Animal*> animals = {
        new Cheetah("Cheetah", 10, "Carnivore", 180),
        new Giraffe("Giraffe", 20, "Herbivore", 1200),
        new Tiger("Tiger", 8, "Carnivore", 300),
        new Elephant("Elephant", 40, "Herbivore", 4500),
        new Lion("Lion", 10, "Carnivore", 200),
        new Alligator("Alligator", 10, "Carnivore", 400),
        new Peacock("Peacock", 10, "Herbivore", 30),
        new Monkey("Monkey", 20, "Herbivore", 40),
        new Eagle("Eagle", 15, "Carnivore", 200),
        new Fish("Fish", 25, "Herbivore", 30)
    };

    for (const auto& animal : animals) {
        animal->DisplayInfo();
    }

    for (const auto& animal : animals) {
        delete animal;
    }

    return 0;
}
