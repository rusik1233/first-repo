import random


word_pairs = {
    'Hi': 'Привет',
    'Bye': 'Пока',
    'Task': 'Задача',
    'Programm': 'Программа',
}



def get_user_mode():
    """ну и управление"""
    while True:
        mode = input("Выбери режим работы тренажера: 0 - добавить новые слова, 1 - тренироваться: \n")
        if mode in ('0', '1'):
            return mode
        print("Недопустимый символ! Выберите 0 или 1.")


def add_word(word_pairs):
    """испарвил добавления слов."""
    while True:
        word = input("Введите слово на русском языке (или нажмите Enter для выхода): ").strip()
        if not word:
            main()

        translation = input("Введите перевод этого слова: ").strip()
        if word and translation:
            word_pairs[translation] = word
            print("Слово успешно добавлено!")
        else:
            print("Ошибка: Введите слово и перевод.")



def play_round(word_pairs):
    """и так понятно"""
    word, translation = random.choice(list(word_pairs.items()))
    answer = input(f"Как переводится слово: {word}? ").strip().lower()
    if answer == translation.lower():
        print("Отлично!!!")
        return 1
    else:
        print(f"Нет... Это слово - {translation}")
        return 0


def train_mode(word_pairs):
    """логика самой игры."""
    score = 0
    print("Переведи как можно больше слов правильно! У тебя 10 попыток!")
    for _ in range(10):
        score += play_round(word_pairs)
    print(f"Твой счет: {score}")



def main():
    """главная функция"""
    mode = get_user_mode()

    if mode == '1':
        train_mode(word_pairs)
    else:
        add_word(word_pairs)


if __name__ == "__main__":
    main()
