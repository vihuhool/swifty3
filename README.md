```
// Enum с разными типами RawValue
enum Day: Int {
    case Monday = 1, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday
}

enum Month: String {
    case January = "Январь", February = "Февраль", March = "Март", April = "Апрель", May = "Май", June = "Июнь", July = "Июль", August = "Август", September = "Сентябрь", October = "Октябрь", November = "Ноябрь", December = "Декабрь"
}

// Enum для анкеты сотрудника
enum Gender {
    case male, female, other
}

enum AgeCategory {
    case child, teenager, adult, senior
}

enum Experience {
    case junior, middle, senior
}

// Enum со всеми цветами радуги
enum RainbowColor {
    case red, orange, yellow, green, blue, indigo, violet
}

// Функция для вывода содержимого enum в консоль
func printEnumContents() {
    let colors: [RainbowColor] = [.red, .orange, .yellow, .green, .blue, .indigo, .violet]
    for color in colors {
        switch color {
        case .red:
            print("apple red")
        case .orange:
            print("orange orange")
        case .yellow:
            print("sun yellow")
        case .green:
            print("leaf green")
        case .blue:
            print("sky blue")
        case .indigo:
            print("deep blue")
        case .violet:
            print("lavender violet")
        }
    }
}

// Функция для выставления оценок ученикам
enum Score: String {
    case excellent = "A", good = "B", satisfactory = "C", needsImprovement = "D", fail = "F"
}

func assignGrade(score: Score) -> Int {
    switch score {
    case .excellent:
        return 5
    case .good:
        return 4
    case .satisfactory:
        return 3
    case .needsImprovement:
        return 2
    case .fail:
        return 1
    }
}

// Метод, который выводит в консоль какие автомобили стоят в гараже
enum Car {
    case sedan, coupe, suv, truck
}

extension Car: CustomStringConvertible {
    var description: String {
        switch self {
        case .sedan:
            return "Седан"
        case .coupe:
            return "Купе"
        case .suv:
            return "Внедорожник"
        case .truck:
            return "Грузовик"
        }
    }
}

func printGarageContents() {
    let garage: [Car] = [.sedan, .coupe, .suv, .truck]
    for car in garage {
        print("В гараже стоит \(car)")
    }
}

// Пример использования функций
printEnumContents()
let grade = Score.good
let numericGrade = assignGrade(score: grade)
print("Оценка \(grade.rawValue) соответствует \(numericGrade)")

printGarageContents()

```
![image](https://github.com/vihuhool/swifty3/assets/69204363/95c9a247-8c0a-438a-aaae-f36bacd3a480)
