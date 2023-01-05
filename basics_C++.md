# tipuri de date
    >> Int ("%d") - 32 bit integer
    >> Long ("%ld") - 64 bit integer
    >> Char ("%c") - character type
    >> Float ("%f") - 32 bit real value
    >> Double ("%lf") - 64 bit real value

    >> citire: scanf(`format specifier`,&val)
    >> afisare: afisare : printf(`format specifier`, val)

# vectori alocati dinamic
    >> int *p = (int*)malloc(n*sizeof(int))
    >> char *p = (char*)malloc(n*sizeof(char))

# re-alocare de memorie
    >> p = (int*)realloc(p, (n+m)*sizeof(int))
    >> p = (char*)realloc(p, (n+m)*sizeof(char))
    >> free(p)

# dimensiunea vectorului
    >> sizeof(p)/sizeof(int)

# matrice alocate dinamic
>>> alocare de memorie
    <<
        void declarare(int** &m, int l, int c){
            m = (int**)calloc(l,sizeof(int*));
            for(int i = 0; i < l; i++)
                m[i] = (int*)calloc(c, sizeof(int));
        }
    >>
    
>>> declarare
    <<
        int **p, l, c;
        void declarare(p, l, c);
    >>

>>> eliberare memorie
    <<
        for(int = 0; i < l; i++)
            free(p[i]);
        free(p);
    >>

# operatii pe fisiere
    >> r - deschidere fisier pentru a fi citit
    >> w - creaza fisier text pentru scriere
    >> a - adauga intr-un fisier text la final
    >> rb - deschide fisier binar pentru citire
    >> wb - creeaza fisier binar pentru scriere
    >> ab - adauga la finalul unui fisier binar
    >> r+ - deschide un fisier pentru citire/scriere
    >> w+ - creeaza un fisier pentru citire/scriere
    >> a+ - adauga in sau creeaza un fisier pentru citire/scriere
    >> r+b - deschide un fisier binar pentru scriere/citire
    >> a+b - adauga sau creeaza un fisier binar pentru scriere/citire