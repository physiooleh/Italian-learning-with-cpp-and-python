#include <iostream>
#include <string>

using namespace std;

struct Question {
    string sentence;      // zdanie z luką
    string correctAnswer; // poprawna forma congiuntivo imperfetto
};

int main() {
    Question quiz[] = {
        {"I miei amici volevano che io (andare)", "andassi"},
        {"Era proprio necessario che loro (chiedere)", "chiedessero"},
        {"I tifosi speravano che la loro squadra (vincere)", "vincesse"},
        {"Le dispiaceva che voi (andare)", "andaste"},
        {"Da bambino pensavo che le zebre (essere)", "fossero"},
        {"Era giusto che anche voi (mangiare)", "mangiaste"},
        {"Temevamo che l'estate (finire)", "finisse"},
        {"Immaginavi che lui (arrivare)", "arrivasse"},
        {"Pensavo che il suo cavallo (avere)", "avesse"},
        {"Credevi che la Terra (essere)", "fosse"},
        {"Desiderava che anche voi (potere)", "poteste"},
        {"Immaginavate che noi (volere)", "volessimo"},
        {"Temeva che lui (dovere)", "dovesse"},
        {"Desideravo che lei (assaggiare)", "assaggiasse"},
        {"Avevamo mangiato un panino prima che (suonare)", "suonasse"},
        {"Era sbagliato che loro (dare)", "dassero"},
        {"Vorrei che voi (studiare)", "studiaste"}
    };

    int numQuestions = sizeof(quiz)/sizeof(quiz[0]);
    string answer;
    bool correct;

    cout << "Quiz: Congiuntivo Imperfetto\n\n";

    for (int i = 0; i < numQuestions; i++) {
        cout << i+1 << ". " << quiz[i].sentence << ": ";
        cin >> answer; // użytkownik wpisuje odpowiedź

        correct = (answer == quiz[i].correctAnswer);

        if (correct) {
            cout << "True! Corretto.\n\n";
        } else {
            cout << "False! La risposta corretta era: " << quiz[i].correctAnswer << "\n\n";
        }
    }

    cout << "Hai completato il quiz!\n";

    return 0;
}
