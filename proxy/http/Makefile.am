# Makefile.am for Http
#
#  Licensed to the Apache Software Foundation (ASF) under one
#  or more contributor license agreements.  See the NOTICE file
#  distributed with this work for additional information
#  regarding copyright ownership.  The ASF licenses this file
#  to you under the Apache License, Version 2.0 (the
#  "License"); you may not use this file except in compliance
#  with the License.  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.

SUBDIRS = remap

AM_CPPFLAGS = \
  $(iocore_include_dirs) \
  -I$(top_srcdir)/proxy/api/ts \
  -I$(top_srcdir)/proxy \
  -I$(top_srcdir)/lib \
  -I$(top_srcdir)/lib/records \
  -I$(top_srcdir)/lib/ts \
  -I$(top_srcdir)/mgmt \
  -I$(top_srcdir)/mgmt/preparse \
  -I$(top_srcdir)/mgmt/utils \
  -I$(top_srcdir)/proxy/hdrs \
  -I$(top_srcdir)/proxy/shared \
  -I$(top_srcdir)/proxy/http/remap \
  -I$(top_srcdir)/proxy/logging \
  -I$(top_srcdir)/proxy/spdy

noinst_HEADERS = HttpProxyServerMain.h
noinst_LIBRARIES = libhttp.a

libhttp_a_SOURCES = \
  HttpAcceptCont.cc \
  HttpAcceptCont.h \
  HttpBodyFactory.cc \
  HttpBodyFactory.h \
  HttpCacheSM.cc \
  HttpCacheSM.h \
  HttpClientSession.cc \
  HttpClientSession.h \
  HttpConfig.cc \
  HttpConfig.h \
  HttpConnectionCount.cc \
  HttpConnectionCount.h \
  HttpDebugNames.cc \
  HttpDebugNames.h \
  HttpPages.cc \
  HttpPages.h \
  HttpProxyServerMain.cc \
  HttpProxyServerMain.h \
  HttpSM.cc \
  HttpSM.h \
  HttpServerSession.cc \
  HttpServerSession.h \
  HttpSessionManager.cc \
  HttpSessionManager.h \
  HttpTransact.cc \
  HttpTransact.h \
  HttpTransactCache.cc \
  HttpTransactCache.h \
  HttpTransactHeaders.cc \
  HttpTransactHeaders.h \
  HttpTunnel.cc \
  HttpTunnel.h \
  HttpUpdateSM.cc \
  HttpUpdateSM.h

if BUILD_TESTS
  libhttp_a_SOURCES += HttpUpdateTester.cc \
    RegressionHttpTransact.cc
endif

#test_UNUSED_SOURCES = \
#  TestHttpTransact.cc \
#  TestUrl.cc \
#  test_socket_close.cc \
#  testheaders.cc
