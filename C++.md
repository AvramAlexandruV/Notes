# vectori alocati dinamic
    >> int *p = (int*)malloc(n*sizeof(int))
    >> char *p = (char*)malloc(n*sizeof(char))

# re-alocare de memorie
    >> p = (int*)realloc(p, (n+m)*sizeof(int))
    >> p = (char*)realloc(p, (n+m)*sizeof(char))

# dimensiunea vectorului
    >> sizeof(p)/sizeof(int)

# matrice alocate dinamic
    <<
        void declarare(int** &m, int l, int c){
            m = (int**)calloc(l,sizeof(int*));
            for(int i = 0; i < l; i++)
                m[i] = (int*)calloc(c, sizeof(int));
        }
    >>
    
    <<
        int **p, l, c;
        void declarare(p, l, c);
    >>

