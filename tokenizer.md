```
text = "Suppose you have a large corpus containing 10 sentences.
        You can create a vocabulary from these sentences by considering only the unique words.
        Then, you can apply a tokenizer to convert each of these unique words into vector representations."

chars = sorted(list(set(text)))
vocab_size = len(chars)
print(''.join(chars))
print(vocab_size)

stoi = {ch:i for i, ch in enumerate(chars)}
print(stoi)
itos = {i:ch for i, ch in enumerate(chars)}
print(itos)

encode = lambda s: [stoi[c] for c in s]
decode = lambda l: ''.join([itos[d] for d in l])

print("\n")
print(encode("hi there"))
print(decode(encode("hi there")))
```
