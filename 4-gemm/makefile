# gpu architecture
sm=80
GENCODE_SM   = -gencode arch=compute_$(sm),code=sm_$(sm)
GENCODE_COMP = -gencode arch=compute_$(sm),code=compute_$(sm)

LDLIBS = -lcublas

all:
	nvcc ${GENCODE_SM} ${GENCODE_COMP} gemm.cu -o gemm ${LDLIBS}

clean:
	del /q gemm.exe gemm.lib gemm.exp