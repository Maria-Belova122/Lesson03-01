# Задание по теме "Пространство имён"

calls = 0


def count_calls():
    global calls
    calls = calls + 1


def string_info(string):
    count_calls()
    tuple_ = (len(string), string.upper(), string.lower())
    return tuple_


def is_contains(string, list_to_search):
    count_calls()
    result = False
    for i in range(len(list_to_search)):
        element_list = str(list_to_search[i])
        if string.upper() == element_list.upper():
            result = True
            break
    return result


print(string_info('Hello'))
print(string_info('Александр'))
print(string_info('b1b’'))
print(is_contains('Hello', ['Hello, Alex', 1.2, 'HeLlO', (3, 4), 'Alex']))
print(is_contains('b1b', ['A1a', 'b1a' 'bbb', 'B1bb']))
print(calls)
