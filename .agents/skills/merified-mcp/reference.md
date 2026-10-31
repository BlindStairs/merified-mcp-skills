# Merified MCP reference

What each group of tools is for and how it writes, what the server does not cover, and the app's words in each language.

## Context and confirmed writes

| The person wants to… | Tool | How it writes |
|---|---|---|
| Know which companies, teams and capabilities they can use | `Merified:get_merified_context` | Read only |
| Carry out a write they confirmed | `Merified:execute_prepared_action` | Runs the plan the person confirmed, unchanged |

## Time tracking

| The person wants to… | Tool | How it writes |
|---|---|---|
| See the work tags they can choose | `Merified:list_my_work_tags` | Read only |
| See worked sessions and planned time per day | `Merified:get_worked_hours_report_data` | Read only |
| Clock in or out now | `Merified:start_my_work_session`, `Merified:end_my_work_session` | At once, at server time; never backdated |
| Fix a clock-in or clock-out | `Merified:prepare_time_correction_request` | Preview, then the person confirms |

Extra time is time worked beyond the plan and already counts; «not reviewed» never means «not counted». With flexible or hourly schedules it is measured per week, Monday to Sunday, so do not add up daily overruns.

Not in this server: reviewing extra time, the hours bank and its payouts, closing a month, pending days, editing the team's daily records, the time control page and its export. Point the person to the Merified app.

## Time off

| The person wants to… | Tool | How it writes |
|---|---|---|
| See their time-off balance and requests | `Merified:get_my_time_off_context` | Read only |
| Find good dates for a number of days off | `Merified:recommend_time_off_windows` | Read only: options, never a request |
| Request time off | `Merified:prepare_time_off_request` | Preview, then the person confirms |

## Team and approvals

| The person wants to… | Tool | How it writes |
|---|---|---|
| Know how many people of a team are available in a period | `Merified:get_team_availability_summary` | Read only |
| Know how many approvals are waiting | `Merified:get_pending_approvals_summary` | Read only |
| See the approvals waiting for them | `Merified:list_pending_approvals` | Read only |
| Approve or reject a request | `Merified:prepare_approval_decision` | Preview, then the person confirms |

## Hiring

| The person wants to… | Tool | How it writes |
|---|---|---|
| Know which vacancies need attention | `Merified:get_recruiting_attention` | Read only |
| See how many candidates are at each stage, for the company or one vacancy | `Merified:get_job_pipeline` | Read only |
| Compare two to five shortlisted applications for one vacancy | `Merified:compare_candidate_shortlist` | Read only |
| Get a short brief of one application | `Merified:get_candidate_brief` | Read only |
| Draft a vacancy that stays inactive | `Merified:prepare_inactive_job` | Preview, then the person confirms |

## The app's words by language

Use these words in the person's language. A dash means the word is not settled in that language yet.

| en | ca | de | es | fr | it | nl | pt |
|---|---|---|---|---|---|---|---|
| hours bank | bossa d'hores | Stundenkonto | bolsa de horas | banque d'heures | banca ore | urenbank | banco de horas |
| clock-in | fitxatge | stempeln | fichaje | pointage | timbratura | inklokken | registo de ponto |
| time off | absència | Abwesenheit | ausencia | absence | assenza | verlof | ausência |
| vacation | vacances | Urlaub | vacaciones | congés | ferie | vakantie | férias |
| absence | absència | Abwesenheit | ausencia | absence | assenza | afwezigheid | ausência |
| vacancy | vacant | Stelle | vacante | poste vacant | posizione aperta | vacature | vaga |
| candidate | persona candidata | Kandidat | persona candidata | personne candidate | persona candidata | kandidaat | pessoa candidata |
| application | candidatura | Bewerbung | candidatura | candidature | candidatura | sollicitatie | candidatura |
| work center | centre de treball | Arbeitsstätte | centro de trabajo | centre de travail | sede di lavoro | werkplek | centro de trabalho |
| manager | gestor | manager | gestor | gestionnaire | responsabile | manager | gestor |
| contract | contracte | Vertrag | contrato | contrat | contratto | contract | contrato |
| payment provider | proveïdor de pagaments | Zahlungsanbieter | proveedor de pagos | prestataire de paiement | fornitore di pagamenti | betaalprovider | fornecedor de pagamentos |
| time tracking | — | — | fichaje | — | — | — | — |
| — | — | — | registro de jornada | — | — | — | — |
| work session | sessió | Arbeitssitzung | sesión | session | sessione | werksessie | sessão |
| workday | jornada | Arbeitstag | jornada | journée de travail | giornata | werkdag | dia de trabalho |
| extra time | temps extra | Mehrzeit | tiempo extra | temps supplémentaire | tempo extra | extra tijd | tempo extra |
| overtime | hores extra | Überstunden | horas extra | heures supplémentaires | straordinario | overuren | horas extra |
| not reviewed | sense revisar | nicht geprüft | sin revisar | non examiné | non esaminato | niet beoordeeld | por rever |
| correction | correcció | Korrektur | corrección | correction | correzione | correctie | correção |
| pending day | dia pendent | offener Tag | día pendiente | jour en attente | giorno in sospeso | openstaande dag | dia pendente |
| shift | torn | Schicht | turno | service | turno | dienst | turno |

«Overtime» means only the paid hours. Time worked beyond the plan is extra time, and it already counts as worked, reviewed or not.

## Words to avoid

Words the app does not use for one meaning, with the word to use instead. Each word is avoided only when it has that meaning.

| Language | When it means | Avoid | Use instead |
|---|---|---|---|
| en | hours bank | bank of hours | hours bank |
| ca | hours bank | borsa d'hores | bossa d'hores |
| de | hours bank | Zeitkonto | Stundenkonto |
| es | hours bank | tiempo compensatorio | bolsa de horas |
| fr | hours bank | compte d'heures | banque d'heures |
| pt | hours bank | bolsa de horas | banco de horas |
| en | clock-in | punch | clock-in / clock-out |
| en | clock-in | clock records | clock-in / clock-out |
| pt | clock-in | bater ponto | registar o ponto |
| ca | time off | temps lliure | absència / absències |
| de | time off | Freizeit | Abwesenheit |
| es | time off | tiempo libre | ausencia(s) |
| fr | time off | temps libre | congés / absence |
| it | time off | tempo libero | assenza / assenze |
| nl | time off | vrije tijd | verlof / afwezigheid |
| pt | time off | tempo livre | ausência(s) |
| fr | vacation | vacances | congés |
| ca | vacancy | ofertes de feina | vacant |
| de | vacancy | Jobs | Stelle |
| es | vacancy | ofertas de empleo | vacante |
| nl | vacancy | baan | vacature |
| ca | candidate | candidatos | candidats |
| es | application | fechas de aplicación | fecha de candidatura |
| en | work center | offices | work center(s) |
| es | work center | oficinas | centro(s) de trabajo |
| fr | work center | lieux de travail | centre de travail |
| nl | work center | werklocaties | werkplek |
| pt | work center | locais de trabalho | centro de trabalho |
| es | manager | managers | gestor / gestores |
| en | contract | policy | contract(s) |
| pt | workday | jornada | dia de trabalho |
| ca | extra time | temps addicionals | temps extra |
| es | extra time | exceso | tiempo extra |
| es | not reviewed | por confirmar | sin revisar |
| fr | shift | postes | service |
