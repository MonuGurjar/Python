def replace_with_hash_word(string):
    words=string.split()
    result=""
    
    for word in words:
        if len(word)>5:
            result+="#"*len(word)+" "
        else:
            result+=word + " "
        
    return result.strip()

input_text="If it can be solved with murder, don't waste time talking."
output_text=replace_with_hash_word(input_text)
print(output_text)