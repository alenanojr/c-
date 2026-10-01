# Aeroworks Interview Lab

I-click, i-type, at panoorin kung ano ang nangyayari. Mas mabilis tumatak kapag ikaw ang gumagalaw.

## 1. Big picture

I-click ang bawat layer. Isipin mo ang app bilang restaurant.

**Say this:** "User → WPF View → ViewModel → C# Service → Database / API / Hardware, and the result returns to the UI through data binding."

## 2. MVVM lab

Ang View ay naka-bind sa ViewModel. I-type ang pangalan, i-click Add. Tapos i-off ang `INotifyPropertyChanged` at tingnan kung ano ang masisira.

**View (XAML)**

Employees: **0**

**ViewModel (C#)**

```

```

[x] INotifyPropertyChanged ON (SetProperty → OnPropertyChanged)

```
public ICommand AddCommand => new RelayCommand(_ => Add(), _ => !string.IsNullOrWhiteSpace(NewName)); // CanExecute
```

**Say this:** "The View binds to the ViewModel through INotifyPropertyChanged and ICommand, so UI and business logic stay decoupled and the ViewModel can be unit-tested without a window."

## 3. SQL JOIN lab

Palitan ang JOIN type at tingnan kung aling rows ang lumalabas.

**Employees**

| Id | Name | Salary | DepartmentId |
| --- | --- | --- | --- |
| 1 | Alberto | 30000 | 1 |
| 2 | Maria | 35000 | 2 |
| 3 | Jose | 28000 | 2 |
| 4 | Ana | 32000 | NULL |

**Departments**

| Id | DepartmentName |
| --- | --- |
| 1 | Firmware |
| 2 | Software |
| 3 | HR |

Min salary

```

```

**Say this:** "INNER returns only matches. LEFT returns every row from the left table and NULLs where there is no match. I use parameterized queries to prevent SQL injection."

## 4. REST + JSON lab

Pumili ng request, i-click Send, at basahin ang response.

[x] Send auth token

Wala pang response.

**Say this:** "GET reads, POST creates, PUT replaces, PATCH updates part of it, DELETE removes. In C# I deserialize the JSON into a model and bind it to a DataGrid."

## 4b. STM32 → C# serial lab

Ang UART ay puwedeng magpadala ng putol-putol na data. I-click ang "Next chunk" at tingnan kung bakit kailangan ng buffer at terminator.

[x] Buffer until "\\n"

**COM3 raw chunks**

—

**Buffer**

—

**C# result**

—

**Common bug:** ang `DataReceived` ay tumatakbo sa background thread. Gamitin ang `Dispatcher.Invoke` bago i-update ang UI-bound property, at `InvariantCulture` sa `double.TryParse`.

## 5. Git flow lab

Pindutin ang mga button nang sunod-sunod: edit → add → commit → push.

## 6. Quiz

Hindi kasama dito ang buong coverage ng C#/OOP, EF Core, Figma, at AI/LLM. Nasa PDF reviewer ang mga iyon, kasama ang code.