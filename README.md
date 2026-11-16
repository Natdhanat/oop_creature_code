# Creature Battle Project (OOP + Git Branching Practice)

This project is designed to help me learn **object-oriented programming**
in Python — especially **inheritance** — while also practicing key **Git
concepts** like branching, merging, conflict resolution, and version history.

I will begin with a base class (`Creature`) and create additional subclasses
on separate Git branches to simulate a real development workflow.

---

## Learning Objectives

### Python / OOP
- Understand and implement **classes**
- Use **inheritance** to extend behaviors
- Override and extend methods (e.g., `attack()`)
- Practice writing simple test code in `main`

### Git / Version Control
- Create and switch branches
- Merge branches into `main`
- Resolve merge conflicts
- View commit history (`git log --graph --all`)

---

## Project Structure

```
oop_creature_code/
│
├── creature_simulation.py   # Base class + subclasses + test code
└── README.md
```

Classes in `creature_simulation.py`:

- `Creature`: base class with `name`, `hp`, `attack_power`, and the methods
  `attack(target)`, `is_alive()`
- `FlyingCreature(Creature)`: adds `altitude`, `fly_to()`, and an `attack()`
  that swoops down from above (branch `flying_creature`)
- `SwimmingCreature(Creature)`: adds `depth`, `dive_to()`, and an `attack()`
  that strikes from underwater (branch `swimming_creature`)
- `FireCreature(Creature)`: adds `fire_level` (0-100), `emit_fire()`, and an
  `attack()` whose damage grows with the fire level (branch `fire_creature`)

---

## How to Test and Run

1. Make sure Python 3 is installed.
2. Open a terminal in the `oop_creature_code` folder.
3. Run:

```
python creature_simulation.py
```

The test code at the bottom of the file (inside `if __name__ == "__main__":`)
prints the results of each test, grouped as:

- Creature Class Tests
- FlyingCreature Tests
- SwimmingCreature Tests
- FireCreature Tests

Each line shows the expected value and the actual value, so you can check
that they match.

To view the branching history:

```
git log --all --graph --oneline
```