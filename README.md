i don't know why we had to fill a read me file so i will just copy paste what i wrote in my algo file.
also just a question, here :         
IF (ch = 'a' OR ch = 'e' OR ch = 'i' OR ch = 'o' OR ch = 'u' OR
    ch = 'A' OR ch = 'E' OR ch = 'I' OR ch = 'O' OR ch = 'U') THEN
    vowels := vowels + 1
    END_IF
was there a way to put both both lowercase and uppercase vowel in one =, i wasnt sure and didnt want to gamble since the checkpoint marked.
another question: 
        IF (ch = ' ') THEN
            words := words + 1
        END_IF
Here I purposely left a space after the word 'algorithm' so I could count it as a word. But let's say I did 'algorithm.' instead, it would have counted 2 words instead of 3, right?


Checkpoint :
ALGORITHM sentence_analysis
VAR
    ch : CHAR;
    length : INTEGER := 0;
    words : INTEGER := 0;
    vowels : INTEGER := 0;
BEGIN
    Read(ch)
    
    WHILE (ch <> '.') DO
        length := length + 1
        
        IF (ch = 'a' OR ch = 'e' OR ch = 'i' OR ch = 'o' OR ch = 'u' OR
            ch = 'A' OR ch = 'E' OR ch = 'I' OR ch = 'O' OR ch = 'U') THEN
            vowels := vowels + 1
        END_IF
        
        IF (ch = ' ') THEN
            words := words + 1
        END_IF

        Read(ch)
    END_WHILE
    
    words := words + 1
    
    Write("Length of sentence: ", length)
    Write("Number of words: ", words)
    Write("Number of vowels: ", vowels)
END

// Example: for "i hate algorithm ." the results would be:
// Length: 16, Words: 3, Vowels: 6
