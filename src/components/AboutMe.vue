<template>
  <section>
    <div class="container px-4 py-5" id="icon-grid">
      <h2 class="pb-2 border-bottom" style="font-family: 'Padauk', sans-serif;">About me</h2>

      <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4 py-5">
        <div class="col d-flex align-items-start" v-for="element in FirstList" :key="element">
          <div class="d-flex align-items-center">
            <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 10px;" width="1.75em" height="1.75em"
                 fill="currentColor" class="bi bi-person" viewBox="0 0 16 16">
              <path
                  d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4zm-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664h10z"/>
            </svg>
            <h3 class="fw-bold mb-0 fs-4 fontfam">{{ element.head_title }}</h3>

          </div>
          <div>
            <p>
            <ul class="personal-ul">
              <li class="personal-li">
                <a style="font-weight: bold">{{ element.name_surname }}</a>

              <li>
                <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                     fill="currentColor" class="bi bi-calendar" viewBox="0 0 16 16">
                  <path
                      d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"/>
                </svg>
                <a>{{ element.date_birth }}</a>
              </li>

              <li>
                <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                     fill="currentColor" class="bi bi-geo-alt" viewBox="0 0 16 16">
                  <path
                      d="M12.166 8.94c-.524 1.062-1.234 2.12-1.96 3.07A31.493 31.493 0 0 1 8 14.58a31.481 31.481 0 0 1-2.206-2.57c-.726-.95-1.436-2.008-1.96-3.07C3.304 7.867 3 6.862 3 6a5 5 0 0 1 10 0c0 .862-.305 1.867-.834 2.94zM8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10z"/>
                  <path d="M8 8a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
                </svg>
                <a>{{ element.home_address }}</a>
              </li>

              <li>
                <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                     fill="currentColor" class="bi bi-telephone" viewBox="0 0 16 16">
                  <path
                      d="M3.654 1.328a.678.678 0 0 0-1.015-.063L1.605 2.3c-.483.484-.661 1.169-.45 1.77a17.568 17.568 0 0 0 4.168 6.608 17.569 17.569 0 0 0 6.608 4.168c.601.211 1.286.033 1.77-.45l1.034-1.034a.678.678 0 0 0-.063-1.015l-2.307-1.794a.678.678 0 0 0-.58-.122l-2.19.547a1.745 1.745 0 0 1-1.657-.459L5.482 8.062a1.745 1.745 0 0 1-.46-1.657l.548-2.19a.678.678 0 0 0-.122-.58L3.654 1.328zM1.884.511a1.745 1.745 0 0 1 2.612.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"/>
                </svg>
                <a target="_blank" href="tel:+389 75 208 886">{{ element.tel_number }}</a>
              </li>

              <li>
                <div class="d-flex align-items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-envelope" viewBox="0 0 16 16">
                    <path
                        d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4Zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2Zm13 2.383-4.708 2.825L15 11.105V5.383Zm-.034 6.876-5.64-3.471L8 9.583l-1.326-.795-5.64 3.47A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.741ZM1 11.105l4.708-2.897L1 5.383v5.722Z"/>
                  </svg>
                  <a target="_blank" href="mailto:ljubomirdavitkov14@gmail.com">{{ element.email }}</a>
                </div>
              </li>

              <li>
                <div class="d-flex align-items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-linkedin" viewBox="0 0 16 16">
                    <path
                        d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z"/>
                  </svg>
                  <a target="_blank" href="https://www.linkedin.com/in/ljubomir-davitkov-0059a1231/">{{
                      element.linkedin
                    }}</a>
                </div>
              </li>

              <li>
                <div class="d-flex align-items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
                    <path
                        d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
                  </svg>
                  <a target="_blank" href="https://github.com/LjupcheD14">{{ element.github }}</a>
                </div>
              </li>

              <li>
                <div class="d-flex align-items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-facebook" viewBox="0 0 16 16">
                    <path
                        d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
                  </svg>
                  <a target="_blank" href="https://www.facebook.com/davitkov.lj">{{ element.facebook }}</a>
                </div>
              </li>

              <li>
                <div class="d-flex align-items-center">
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-instagram" viewBox="0 0 16 16">
                    <path
                        d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
                  </svg>
                  <a target="_blank" href="https://www.instagram.com/davittkov/">{{ element.instagram }}</a>
                </div>
              </li>

              </li>
            </ul>
            </p>
          </div>
        </div>

        <div class="col d-flex align-items-start" v-for="element in SecondList" :key="element">
          <div class="d-flex align-items-center">
            <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 10px;" width="1.75em" height="1.75em"
                 fill="currentColor" class="bi bi-briefcase" viewBox="0 0 16 16">
              <path
                  d="M6.5 1A1.5 1.5 0 0 0 5 2.5V3H1.5A1.5 1.5 0 0 0 0 4.5v8A1.5 1.5 0 0 0 1.5 14h13a1.5 1.5 0 0 0 1.5-1.5v-8A1.5 1.5 0 0 0 14.5 3H11v-.5A1.5 1.5 0 0 0 9.5 1h-3zm0 1h3a.5.5 0 0 1 .5.5V3H6v-.5a.5.5 0 0 1 .5-.5zm1.886 6.914L15 7.151V12.5a.5.5 0 0 1-.5.5h-13a.5.5 0 0 1-.5-.5V7.15l6.614 1.764a1.5 1.5 0 0 0 .772 0zM1.5 4h13a.5.5 0 0 1 .5.5v1.616L8.129 7.948a.5.5 0 0 1-.258 0L1 6.116V4.5a.5.5 0 0 1 .5-.5z"/>
            </svg>
            <h3 class="fw-bold mb-0 fs-4 fontfam">{{ element.head_title }}</h3>

          </div>
          <div>
            <p>
            <ul class="personal-ul">
              <li class="personal-li">
                <a style="font-weight: bold">{{ element.sub_title }}</a>


              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>{{ element.company }}</a>
                <ul class="personal-ul-second">
                  <li>
                    <a>{{ element.position }}</a>
                  </li>
                  <li>
                    <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                         fill="currentColor" class="bi bi-calendar" viewBox="0 0 16 16">
                      <path
                          d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"/>
                    </svg>
                    <a>{{ element.date }}</a>
                  </li>
                </ul>
              </li>


              </li>
              <li>
                <a style="font-weight: bold">{{ element.head_title_2 }}</a>

              <li v-for="experince in Experinces" :key="experince">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>{{ experince }}</a>
              </li>
            </ul>
            </li>

            </p>
          </div>
        </div>

        <div class="col d-flex align-items-start">
          <div class="d-flex align-items-center">
            <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 10px;" width="1.75em" height="1.75em"
                 fill="currentColor" class="bi bi-book" viewBox="0 0 16 16">
              <path
                  d="M1 2.828c.885-.37 2.154-.769 3.388-.893 1.33-.134 2.458.063 3.112.752v9.746c-.935-.53-2.12-.603-3.213-.493-1.18.12-2.37.461-3.287.811V2.828zm7.5-.141c.654-.689 1.782-.886 3.112-.752 1.234.124 2.503.523 3.388.893v9.923c-.918-.35-2.107-.692-3.287-.81-1.094-.111-2.278-.039-3.213.492V2.687zM8 1.783C7.015.936 5.587.81 4.287.94c-1.514.153-3.042.672-3.994 1.105A.5.5 0 0 0 0 2.5v11a.5.5 0 0 0 .707.455c.882-.4 2.303-.881 3.68-1.02 1.409-.142 2.59.087 3.223.877a.5.5 0 0 0 .78 0c.633-.79 1.814-1.019 3.222-.877 1.378.139 2.8.62 3.681 1.02A.5.5 0 0 0 16 13.5v-11a.5.5 0 0 0-.293-.455c-.952-.433-2.48-.952-3.994-1.105C10.413.809 8.985.936 8 1.783z"/>
            </svg>
            <h3 class="fw-bold mb-0 fs-4 fontfam" v-for="element in EducationTitle" :key="element">
              {{
                element.head_title
              }}</h3>
          </div>
          <p>
          <ul class="personal-ul" v-for="element in Education" :key="element">
            <li>
              <a style="font-weight: bold">{{ element.title }}</a>
            </li>
            <li>
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                   viewBox="0 0 16 16">
                <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
              </svg>
              <a>{{ element.name }}</a>
              <ul class="personal-ul-second">
                <li>
                  <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 5px" width="16" height="16"
                       fill="currentColor" class="bi bi-calendar" viewBox="0 0 16 16">
                    <path
                        d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"/>
                  </svg>
                  <a>{{ element.date }}</a>
                </li>
              </ul>
            </li>
          </ul>

          </p>
        </div>


        <div class="col d-flex align-items-start">
          <div class="d-flex align-items-center">
            <svg xmlns="http://www.w3.org/2000/svg" style="margin-right: 10px;" width="1.75em" height="1.75em"
                 fill="currentColor" class="bi bi-laptop" viewBox="0 0 16 16">
              <path
                  d="M13.5 3a.5.5 0 0 1 .5.5V11H2V3.5a.5.5 0 0 1 .5-.5h11zm-11-1A1.5 1.5 0 0 0 1 3.5V12h14V3.5A1.5 1.5 0 0 0 13.5 2h-11zM0 12.5h16a1.5 1.5 0 0 1-1.5 1.5h-13A1.5 1.5 0 0 1 0 12.5z"/>
            </svg>
            <h3 class="fw-bold mb-0 fs-4 fontfam">Skills</h3>

          </div>
          <div>
            <p>
            <ul class="personal-ul">

              <li>
                <a>Communicative</a>
              </li>

              <li>
                <a>Initiative</a>
              </li>

              <li>
                <a>Team player</a>
              </li>

              <li>
                <a>Adjustable</a>
              </li>

              <li>
                <a style="font-weight: bold">Programming</a>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>C, C++, C#, Java, SQL</a>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>Object-oriented concept</a>
              </li>

              <li>
                <a style="font-weight: bold">Web development</a>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>HTML, CSS, Javascript, Vue, Git</a>
              </li>

              <li>
                <a style="font-weight: bold">Languages</a>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>English (fluent)</a>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-dot"
                     viewBox="0 0 16 16">
                  <path d="M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
                </svg>
                <a>Macedonian (native)</a>
              </li>

            </ul>

            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutMe",
  data() {
    return {
      FirstList: [
        {
          head_title: "Personal",
          name_surname: "Ljubomir Davitkov",
          date_birth: "14.08.2002",
          home_address: "Pitu Guli 7/a, Kochani, Macedonia",
          tel_number: "+389 75 208 886",
          email: "Email",
          linkedin: "LinkedIn",
          github: "GitHub",
          facebook: "Facebook",
          instagram: "Instagram"
        }
      ],
      SecondList: [
        {
          head_title: "Experince",
          sub_title: "Professional experince",
          company: "Bike Computer",
          position: "Web developer Intern",
          date: "July, 2022 - Present",
          head_title_2: "Youth activism"
        }
      ],
      Experinces: [
        'Karate athlete',
        'Red cross',
        'Scout',
        'Member of non-governmental organizations',
        'Youth international exchanges'
      ],
      EducationTitle: [
        {
          head_title: "Education"
        }
      ],
      Education: [
        {
          title: "University",
          name: "Faculty of Informatics Sciences and Computer Engineering – Skopje",
          date: "2021 - Present"
        },
        {
          title: "High School",
          name: "Mihajlo Pupin - Skopje",
          date: "2017 - 2021"
        }
      ],
      Skills: ['Communicative', 'Initiative', 'Team player', 'Adjustable']
    }
  }
}
</script>

<style scoped>

</style>
