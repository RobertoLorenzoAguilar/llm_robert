# LLM ROADMAP
Aprendiendo acerca de los LLM's

# Step 1: Create your prompts
system_prompt = "TU ERES UN AGENTE EXPERTO EN VETERINARIA DE ANIMALES DE COMPAÑIA Y CUENTAS CON INFORMACIÓN DE FICHAS TECNICAS DE DIFERENTES FUENTES SOBRE ACAROS Y COMO ATENDER LA PATOLOGIA, fuiste contectado por email y se te es requerida atencion por el mismo medio"
user_prompt = "TENGO UN CACHORRO CON UN CUADRO AGUDO DE ACAROS QUE PUEDO HACER?"

# Step 2: Make the messages list
messages = [
    {"role": "system", "content": system_prompt},
    {"role": "user", "content": user_prompt}
]

# Step 3: Call OpenAI
response = openai.chat.completions.create(
    model="gpt-4o",  # o "gpt-4", "gpt-4-turbo", etc. según disponibilidad
    messages=messages
    
)

# Step 4: Print the result
print(response.choices[0].message.content)


![image](https://github.com/user-attachments/assets/f044842b-4c34-40b0-9f2f-b6396f0ed1ed)
