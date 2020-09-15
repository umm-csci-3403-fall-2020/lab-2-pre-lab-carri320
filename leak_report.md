# Leak report

The memory leak was in the cleaned variable of the is_clean function. To fix the issue put free(clean); in the line before return result == 0; still inside the is_clean function. This works because the line above result = strcmp(str, cleaned); is the last time that the cleaned variable is used. 
