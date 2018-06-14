#
#  Copyright (c) 2016-2017, The OpenThread Authors.
#  All rights reserved.
#
#  Redistribution and use in source and binary forms, with or without
#  modification, are permitted provided that the following conditions are met:
#  1. Redistributions of source code must retain the above copyright
#     notice, this list of conditions and the following disclaimer.
#  2. Redistributions in binary form must reproduce the above copyright
#     notice, this list of conditions and the following disclaimer in the
#     documentation and/or other materials provided with the distribution.
#  3. Neither the name of the copyright holder nor the
#     names of its contributors may be used to endorse or promote products
#     derived from this software without specific prior written permission.
#
#  THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
#  AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
#  IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
#  ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
#  LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
#  CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
#  SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
#  INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
#  CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
#  ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
#  POSSIBILITY OF SUCH DAMAGE.
#

include $(abs_top_nlbuild_autotools_dir)/automake/pre.am

LOG_DRIVER=$(abs_top_srcdir)/third_party/openthread-test-driver/test-driver

EXTRA_DIST                                                         = \
    Cert_5_1_05_RouterAddressTimeout.py                              \
    $(NULL)

check_PROGRAMS                                                     = \
    $(NULL)

check_SCRIPTS                                                      = \
    Cert_5_1_05_RouterAddressTimeout.py                              \
    $(NULL)

TESTS_ENVIRONMENT                                                  = \
    export                                                           \
    top_builddir='$(top_builddir)'                                   \
    VERBOSE=1;                                                       \
    $(NULL)

TESTS                                                              = \
    $(check_PROGRAMS)                                                \
    $(check_SCRIPTS)                                                 \
    $(NULL)

XFAIL_NCP_TESTS                                                    = \
    test_service.py                                                  \
    Cert_5_2_05_AddressQuery.py                                      \
    Cert_5_3_08_ChildAddressSet.py                                   \
    Cert_5_3_09_AddressQuery.py                                      \
    Cert_5_3_10_AddressQuery.py                                      \
    Cert_8_1_01_Commissioning.py                                     \
    Cert_8_1_02_Commissioning.py                                     \
    Cert_8_2_01_JoinerRouter.py                                      \
    Cert_8_2_02_JoinerRouter.py                                      \
    Cert_9_2_04_ActiveDataset.py                                     \
    Cert_9_2_07_DelayTimer.py                                        \
    Cert_9_2_08_PersistentDatasets.py                                \
    Cert_9_2_09_PendingPartition.py                                  \
    Cert_9_2_10_PendingPartition.py                                  \
    Cert_9_2_11_MasterKey.py                                         \
    Cert_9_2_12_Announce.py                                          \
    Cert_9_2_13_EnergyScan.py                                        \
    Cert_9_2_14_PanIdQuery.py                                        \
    Cert_9_2_15_PendingPartition.py                                  \
    Cert_9_2_16_ActivePendingPartition.py                            \
    Cert_9_2_17_Orphan.py                                            \
    Cert_9_2_18_RollBackActiveTimestamp.py                           \
    $(NULL)

XFAIL_TESTS = $(if $(filter $(NODE_TYPE),ncp-sim),$(XFAIL_NCP_TESTS))

include $(abs_top_nlbuild_autotools_dir)/automake/post.am
