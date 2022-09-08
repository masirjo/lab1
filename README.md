students = {}
come = ''
while True:
    come == input('command ')
    if come == 'end':
        break

    if come == "zap":
        count = int(input('Count of Student '))



        for i in range(int(count)):
            while True:
                print(f'\nStudent number {i+1}')
                data = input("Введите данные в формате Math Fizra Economic\n ")
                name, matan, fizra, economic = data.split()


                if 2 <= int(matan) <= 5 and 2 <= int(fizra)<=5 and 2 <= int(economic) <=5:
                    break

                print("Error, type again")

            students[name] = {'Math': int(matan), 'Fizra': int(fizra), 'Economic': int(economic)}

    elif come == 'find':
        name, disciplina = input('Введите данные в формате: name discipline\n').split()
        print(students[name][disciplina])

    elif come == "view":
        print(students)
