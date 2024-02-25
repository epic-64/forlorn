# forlorn
A definition of the forlorn programming language.

Created in collaboration with a RAG-enabled version of GPT4, that is able to make amendmends to the language and read/write forlorn programs. Currently there is no compiler.

Most constructs can be translated directly from other C-like languages.

## Basics
### Defining a variable
```
embody message: Echo = "hello world";
```

### Data Types
```
x: Void = Nothingness; // null pointer
x: Verity = Certain; // boolean true
x: Verity = Doubtful; // boolean false
x: Figure = 5; // number
x: Figure = 3.14; // number
x: Echo = "I ponder, therefore I am"; // string
x: Specter[Echo] = Maybe "I might exist"; // Nullable type
x: Narrative[Echo] = ["In the beginning", "there was code"]; // array
x: Narrative[Specter[Figure]] = [Maybe 5, Maybe 200]; // array
x: Labyrinth[Echo, Figure] = {"first": 3.14, "second": 42}; // map
```

### Printing
```
whisper "Nice day for fishing, ain't it?"
```

### Functions, Conditionals, Return
```
// This function contemplates the modulo
contemplate Remnant(dividend: Figure, divisor: Figure) -> Figure
    embrace dividend - (divisor * (dividend / divisor).floor());
conclude

// This function contemplates the essence of FizzBuzz
contemplate FizzBuzz(number: Figure) -> Echo
    ponder (Remnant(number, 15) is 0)
        embrace "FizzBuzz";
    seek (Remnant(number, 3) is 0)
        embrace "Fizz";
    seek (Remnant(number, 5) is 0)
        embrace "Buzz";
    seek
        embrace number.toString();
    conclude
conclude
```

### For Loop
```
forlornly wander (step=1 until 100)
    whisper FizzBuzz(step);
conclude
```

### Foreach Loop
```
among (thought in thoughts)
    // engage with 'thought'
conclude
```

### Match and raising exceptions
```
embody answer = question Purpose
    Concept.Suffering: embrace "Life is suffering";
    Concept.Happiness: embrace "Happiness is the way";
    Unforeseen: evoke Crisis[UnexpectedPerspective]("Encountered new perspective {Purpose}"); // Unforeseen is a reserved keyword, for unmatched cases
conclude
```

