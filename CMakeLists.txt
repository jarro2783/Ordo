cmake_minimum_required(VERSION 3.27)

project(ordo)

enable_language(CXX)

set(SOURCES
  relprior.c
  namehash.c
  fit1d.c
  gauss.c
  justify.c
  mymem.c
  myopt/myopt.c
  mystr.c
  mytimer.c
  proginfo.c
  ra.c
  randfast.c
  sysport/sysport.c
  xpect.c
  pgnget.c
  groups.c
  indiv.c
  encount.c
  ratingb.c
  rating.c
  csv.c
  report.c
  cegt.c
  plyrs.c
  relpman.c
  myhelp.c
  inidone.c
  rtngcalc.c
  sim.c
  summations.c
  bitarray.c
  strlist.c
  main.c
)

add_executable(ordo ${SOURCES})
target_compile_definitions(ordo PRIVATE MY_SEMAPHORES)
target_include_directories(ordo PRIVATE myopt sysport)
target_compile_options(ordo PRIVATE -g -march=native)

set_source_files_properties(${SOURCES} PROPERTIES LANGUAGE CXX)
